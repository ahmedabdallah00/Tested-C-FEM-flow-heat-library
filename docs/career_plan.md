# Project context: SciML & Simulation Career Plan (Kareem & Ahmed)

Last updated: 15 Nov 2026
Main plan doc: https://claude.ai/artifact/15dveFWzz5KgYz7KxPGAM9 ("SciML & Simulation Career Plan — Kareem & Ahmed")

## Goal
We are two engineers in Cairo, Egypt, preparing for industrial roles in scientific ML, digital twins,
computational engineering and simulation (main target: Siemens Digital Industries Software).
We build skills through hands-on, INDUSTRIAL mini-projects, not academic ones. Every project
must be a usable tool, posted on LinkedIn, and added to both CVs.

## Team
**Kareem Eldesouky:** MSc Aerospace Engineering, Cairo University (Prof. Amr Guaily); Graduate Research
Assistant at AUC.
- Strong: CFD (GPU OpenFOAM with PETSc/AmgX, Fluent reacting flow, SU2 source edits), a C++ GLS FEM
  Navier–Stokes solver written from scratch, PIV experiments, Hilbert POD, MATLAB optimisation.
- Weaker: production software practice (tests, CI, packaging), JAX/CUDA, neural operators, 0D/1D modelling.
- Laptop GPU: NVIDIA T1200 (4 GB, Turing, no tensor cores). Used for C++, OpenFOAM, Modelica and inference.

**Ahmed Algharib:** MSc Autonomous Robotics, Mansoura University; digital twin engineer.
- Strong: modern C++ (17/23), Python, Isaac Sim/Omniverse/OpenUSD/PhysX FEM, MuJoCo, ROS 2,
  PLC/OPC UA, PyTorch, data pipelines (Kafka, InfluxDB, SQL, GCP), Docker.
- Studying: Julia, JAX, SciML (Neural ODE, PINN, UDE), ROM.
- Weaker: CFD and PDE numerics.
- Laptop GPU: RTX 5050 (8 GB). This is the training machine.

## Constraints (confirmed)
- **Time:** 8 hours/week EACH, including one 2-hour joint session per week.
- **Compute:** no HPC. Two laptops plus free cloud GPUs (Kaggle, about 30 GPU-h/week, as the backup).
- **Data:** ready-made public CFD datasets are allowed (e.g., AirfRANS, NVIDIA Ahmed body dataset).
- **Software:** open-source tools only (no STAR-CCM+/Amesim licences).
- **Focus:** industrial, practical experience and agility with new tech. No papers or literature reviews.
- **Fixed deadline:** Kareem's SU2 Foundation application is due 27 Nov 2026. MSc exam dates are not known yet.

## Target roles (from the job descriptions we collected)
- **Tier 1:** Siemens Physics AI / Simcenter ROM (Cairo); Siemens UnityX C++ framework (Cairo);
  Siemens STAR-CCM+ Application Engineer with AI focus (London, needs a referral); Siemens Heat
  Transfer Software Engineer (needs a completed Master's).
- **Tier 2:** Gradient Dynamics founding engineer; Lam Research modeling engineer; Airbus cryogenic H2
  0D/1D simulation and Airbus thermal roles.
- **Tier 3:** NVIDIA differentiable simulation intern (PhD-level).
- **Skip:** US-citizenship/ITAR roles (SpaceX, Mach, TerraPower, Rolls-Royce US).

## Key decisions
- **Stack:** Python (PyTorch + JAX) is the main portfolio language; C++ with pybind11 for one
  framework project; Julia/SciML as a side track for Ahmed only (P4).
- **Pace:** a portfolio-quality project takes about 6 weeks at 8 h/week each, so projects are split into
  2–3 sprints. Every sprint ends in something we can post.
- **One project at a time.** One-week buffers between projects.
- **Every project:** a one-paragraph customer problem, a shippable product (package, service, CLI,
  FMU or dashboard), engineering KPIs, at least one recent industry tool, and a one-page app note.
- **Apply now:** Ahmed applies to the current Siemens Cairo Physics AI posting (posted 9 Nov 2026)
  without waiting for the projects.

## Project portfolio (15 months: 23 Nov 2026 – 27 Feb 2028)
| # | Project | Lead | Weeks | Ships | Main targets |
|---|---|---|---|---|---|
| P1 | Tested C++ FEM flow + heat library with Python bindings (from Kareem's solver) | Ahmed (software) / Kareem (numerics) | 6 | pip package, CI on Windows and Linux; validated vs Ghia and de Vahl Davis | Siemens UnityX, HEAT, Gradient |
| P3 | Agentic OpenFOAM workflow with physics verification gates | Ahmed / Kareem | 5 | CLI + run report; tested on 10 good and 10 broken cases | Siemens AE London, Rolls-Royce digital |
| P2 | Airfoil aero surrogate service with uncertainty (AirfRANS, 1,000 RANS cases) | Kareem / Ahmed | 8 | DVC + MLflow pipeline, ensemble UQ, ONNX + FastAPI + Docker | Siemens Physics AI / ROM, Lam |
| P4 | Cooling-loop 0D/1D model in OpenModelica, FMU co-simulation (FMPy), UDE heat-exchanger correction trained on P1 runs | Kareem / Ahmed | 7 | Sizing app + FMU | Airbus cryo/thermal, Siemens HEAT |
| P5 | Test-data calibration tool on a differentiable JAX thermal model | Kareem / Ahmed | 7 | CLI: test CSV in, parameters with uncertainty out | NVIDIA, Gradient, Lam |
| P6 | Flagship: live thermal digital twin of a desktop rig (heater, fan, thermocouples) | Joint | 12 | Live dashboard; prediction 10 min ahead; fault flag | All Tier 1 + Lam |

Order: Foundations (2 wk) → P1 → P3 → **Gate 1 (28 Feb 2027)** → P2 → P4 → P5 → **Gate 2 (29 Aug 2027)**
→ P6 → polish + applications → **Gate 3 (27 Feb 2028)**.

## Phase gates
- **Gate 1:** 2 repos public with CI; 4 LinkedIn posts; applied to Siemens Physics AI, UnityX and AE London.
- **Gate 2:** 5 repos and 5 app notes public; about 10 posts; applied to Siemens ROM roles and Airbus.
- **Gate 3:** twin demo video public; one merged open-source PR; Tier 2 applications sent.

## Learning resources (verdicts)
- **Core:** NABLA-SciML (PINN/DeepONet tutorials, study only; check the licence before copying code);
  Modelica by Example (Kareem, Phase 1); SciML docs (Ahmed).
- **Attend:** JuliaHub webinar "Rethinking HVAC and Thermal-Fluid Modeling" (Dyad), 18 Nov 2026.
- **Optional:** JuliaHub case studies; Juan Toscano's YouTube channel.

## Branding rules
- One LinkedIn post per finished sprint (about every 3 weeks), alternating authors, about 1 hour each.
- Each post has one picture, one number, the repo link, and one honest limitation.
- CV bullets use the form "action + method + measured result". Only real measured numbers.

## Open decisions
1. Does Ahmed commit to the Julia side track? If not, P4's UDE moves to PyTorch.
2. Budget: P6 rig hardware, and either an LLM API budget for P3 or a decision to use a small local model.
3. Set up a shared GitHub organisation before P1.

## Immediate next steps
- 18 Nov: both attend the webinar.
- Week 1 (23–29 Nov): Kareem finishes the SU2 application. Ahmed sets up the GitHub org and the
  repo template (CMake, pytest, GitHub Actions).
- Week 2 (30 Nov–6 Dec): Kareem works through Modelica by Example; Ahmed does the NABLA-SciML PINN
  module; joint P1 scoping session.
- Now: Ahmed applies to the Siemens Cairo Physics AI posting.

## How Claude should work in this project
- Use the plan doc above as the source of truth; update it rather than starting new plans.
- Keep replies concise; put code in code blocks; Kareem's Python is rusty, so explain steps clearly.
- Don't correct Kareem's English.
- Be honest when a goal is unrealistic for our time or compute.
- If unsure about a library or function name, say so and point to the docs.
