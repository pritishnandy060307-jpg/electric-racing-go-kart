# Initial Requirements Register

Living register. Values are project intentions, not verified vehicle capabilities.

Status: Proposed = requires review; Open = not verified; Verified = objective evidence recorded.

| ID | Category | Requirement / target | Verification method | Status |
|---|---|---|---|---|
| SYS-001 | Configuration | Single-seat electric kart | Architecture review | Proposed |
| SYS-002 | Drivetrain | Rear-wheel drive | CAD/interface inspection | Proposed |
| PERF-001 | Speed | Target envelope 60–80 km/h, subject to feasibility and controlled-test approval | Vehicle model and instrumented closed-course test | Open |
| PERF-002 | Acceleration | Set measurable acceleration targets after mass and motor sizing | Longitudinal model and controlled test | Open |
| PERF-003 | Range | Set range target from intended duty cycle and budget | Energy model and controlled test | Open |
| MASS-001 | Mass | Establish total mass from subsystem mass budget | CAD mass properties and weighing | Open |
| GEO-001 | Packaging | Fit driver, controls, powertrain, battery and safety systems without interference | CAD packaging and physical fit check | Open |
| CHS-001 | Structure | Chassis withstands defined service/test loads with documented margin | Calculations, FEA review and inspection | Open |
| STR-001 | Steering | Steering achieves defined turning geometry and has positive stops | Geometry calculation and inspection | Open |
| BRK-001 | Braking | Braking meets defined stopping performance without exceeding component ratings | Calculation, component review and controlled test | Open |
| PWR-001 | Powertrain | Motor/controller meet continuous and peak torque-speed duty within limits | Datasheets and vehicle model | Open |
| BAT-001 | Energy | Battery meets defined usable energy/current envelope within cell and BMS limits | Cell data, calculations and supervised tests | Open |
| ELEC-001 | Protection | Electrical system has selected overcurrent protection and safe isolation | Schematic review and inspection | Open |
| ELEC-002 | Emergency stop | Driver-accessible emergency shutdown strategy is defined and verified | Architecture review and commissioning test | Open |
| THM-001 | Thermal | Motor, controller, battery, cables and connectors remain within manufacturer limits | Thermal analysis and instrumented test | Open |
| COST-001 | Budget | Total project spend target ₹40,000–₹60,000 | Quoted and actual-cost BOM | Open |
| DOC-001 | Documentation | Released design has drawings, BOM, calculations, assumptions and revision history | Document audit | Open |
| TST-001 | Validation | Progressive test plan defines inspections, abort criteria, instrumentation and controlled conditions | Test-plan review | Open |

## Resolve first

1. Driver design mass and ergonomic envelope.
2. Intended track/use environment and applicable rules.
3. Required range and continuous operating duration.
4. Acceleration and gradient requirements.
5. Maximum-speed requirement and allowable test conditions.
6. Overall mass and packaging constraints.
7. Available fabrication processes and supplier constraints.

For every requirement, record owner, rationale, source, threshold, operating condition, method, acceptance criteria, evidence link, status and revision. Do not mark a requirement verified from an estimate or unvalidated simulation alone.
