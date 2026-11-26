# Electric Racing Go-Kart

Individual engineering project to design a single-seat, rear-wheel-drive electric racing go-kart. This repository documents requirements, benchmarking, mechanical design, powertrain sizing, electrical architecture, CAD, simulation, manufacturing documentation, and validation.

> **Status:** Concept development / requirements definition  
> **Target speed:** 60–80 km/h, subject to feasibility and safety validation  
> **Budget target:** ₹40,000–₹60,000

## Project objectives

- Develop an integrated vehicle architecture and subsystem interfaces.
- Design chassis, steering, front assembly, rear axle, drivetrain, and brakes.
- Size motor, controller, battery, and protection system from calculated requirements.
- Build a complete SOLIDWORKS assembly and drawing package.
- Verify critical structures and vehicle performance using ANSYS and MATLAB/Simulink.
- Prepare a costed bill of materials and controlled manufacturing/test plan.

## Preliminary targets

These are targets, not verified capabilities or released specifications.

| Parameter | Preliminary target |
|---|---|
| Configuration | Single-seat electric kart |
| Drive | Rear-wheel drive |
| Maximum speed | 60–80 km/h; feasibility to be demonstrated |
| Motor | BLDC/PMSM candidate; size from wheel-force and duty-cycle requirements |
| Battery bus | 60–72 V candidate; subject to component and safety review |
| Transmission | Chain drive candidate |
| Chassis | Welded tubular steel candidate |
| Braking | Hydraulic disc system candidate |
| Budget | ₹40,000–₹60,000; vendor quotations required |

## Engineering workflow

1. Research and benchmark comparable karts and components.
2. Define measurable requirements, assumptions, interfaces, and mass budget.
3. Establish geometry, packaging, axle loads, centre of gravity, and performance feasibility.
4. Design mechanical and electrical subsystems.
5. Complete traceable engineering calculations.
6. Build and integrate the CAD model.
7. Verify using structural and vehicle performance simulations.
8. Review and freeze the design before fabrication.
9. Prepare released drawings, BOM, fabrication and inspection plans.
10. Conduct controlled, progressive validation after safety review.

## Repository map

- `docs/` — project plan, requirements, architecture, design decisions
- `research/` — benchmarking, references, component database
- `calculations/` — vehicle dynamics, powertrain, braking, steering, chassis, electrical
- `cad/` — SOLIDWORKS parts, assemblies, drawings, neutral exports
- `simulations/` — ANSYS and MATLAB/Simulink models and reports
- `electrical/` — battery, wiring, protection documentation
- `manufacturing/` — released drawings, BOM, fabrication and inspection
- `testing/` — test plans, inspections, raw data and results
- `reports/` — design reviews and final technical report

## Getting started

1. Read [the project plan](docs/project-plan.md).
2. Review [the requirements register](docs/requirements.md).
3. Review [the vehicle architecture](docs/vehicle-architecture.md).
4. Establish the master layout using [the geometry and packaging baseline](docs/geometry-and-packaging.md).
5. Start with benchmarking, a source register, and a first-pass mass budget.
6. Record unresolved choices in [the design decision log](docs/design-decisions/README.md).

## Engineering rules

- Record assumptions, units, sources, revisions, and methods.
- Distinguish **target**, **predicted**, **simulated**, and **measured** values.
- Select components only after deriving the operating envelope and reviewing datasheets.
- Do not release parts for fabrication before interface and safety reviews.
- Validate FEA boundary conditions, material data, and mesh sensitivity.
- Never trade away steering, braking, electrical protection, or structural integrity to meet cost.
- Separate vendor estimates, confirmed quotations, and actual expenditure.
- Do not commit credentials, private data, caches, or unreviewed binary exports.

## Tools

- SOLIDWORKS — mechanical CAD and assemblies
- ANSYS — structural and modal analysis
- MATLAB / Simulink — vehicle and powertrain models
- Git / GitHub — revision control, issues, milestones, and reviews

## Safety notice

This repository is engineering documentation, not a construction or operating approval. A high-speed kart can cause severe injury. Before fabrication or powered testing, obtain competent engineering review of the chassis, steering, brakes, restraints, tyres, electrical system, battery enclosure, and emergency isolation. Use properly rated components, suitable protective equipment, a controlled closed test area, and qualified supervision. Battery assembly and high-current electrical work require appropriate training and safeguards. Comply with applicable venue, competition, and legal requirements.

## Licensing

The existing `LICENSE` governs material covered by it. Third-party CAD, images, datasheets, software, and references remain subject to their own licenses and terms.
