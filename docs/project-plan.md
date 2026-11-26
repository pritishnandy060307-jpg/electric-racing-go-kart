# Complete Engineering Design & Development Plan

**Vehicle:** Single-seat, rear-wheel-drive electric racing go-kart  
**Target speed:** 60–80 km/h, subject to feasibility validation  
**Budget target:** ₹40,000–₹60,000  
**Tools:** SOLIDWORKS, ANSYS, MATLAB/Simulink

## 1. Purpose

Deliver an integrated, manufacturing-ready design package. The design phase covers research, requirements, vehicle sizing, subsystem design, calculations, CAD, simulation, manufacturing documentation, cost control, and a safe validation plan. Fabrication and physical testing are separate activities, gated by design and safety reviews.

## 2. Stage-gate workflow

| Gate | Work | Exit evidence |
|---|---|---|
| G0 Research | Benchmark karts; collect datasheets and applicable rules | Benchmark matrix and source register |
| G1 Requirements | Define operating envelope, performance, safety, budget, verification | Reviewed requirements register |
| G2 Vehicle concept | Layout, mass budget, geometry, architecture | Concept review and interface map |
| G3 Subsystems | Chassis, steering, axle, drivetrain, brakes, powertrain, battery | Subsystem calculations and CAD |
| G4 Analysis | Structural, performance, electrical and thermal checks | Reviewed analysis report |
| G5 Integration | Complete CAD, clearance, serviceability, mass/cost reconciliation | Integrated design review |
| G6 Release | Drawings, BOM, fabrication and inspection plan | Released manufacturing package |
| G7 Validation | Static inspection, commissioning, progressive controlled tests | Test records and closure report |

Progress is determined by exit evidence, not simply elapsed time.

## 3. Phase-by-phase plan

### Phase 1 — Research and benchmarking (Week 1)
- Benchmark electric racing karts and chassis configurations.
- Record mass, wheelbase, track, tyres, motor, controller, battery, gearing, brakes and published performance.
- Obtain manufacturer datasheets for candidate components.
- Record source URLs, revisions, access dates, units, and whether values are manufacturer-published or estimates.
- Identify rules and test-site constraints relevant to the intended vehicle.

**Outputs:** benchmark spreadsheet, source register, component shortlist.

### Phase 2 — Requirements and architecture (Week 2)
- Define driver design mass, duty cycle, range, acceleration, speed, gradient, environment and budget.
- Create measurable functional, performance, packaging, reliability, maintainability and safety requirements.
- Draw mechanical power flow, electrical energy flow, control interfaces and emergency isolation architecture.
- Create an interface register covering mounts, loads, dimensions, voltage/current, cooling and service access.
- Assign a verification method to every requirement.

**Outputs:** requirements register, architecture diagram, interface register, risk register.

### Phase 3 — Vehicle sizing and packaging (Week 2)
- Establish coordinate system and preliminary wheel/tyre envelope.
- Select candidate wheelbase, track, ground clearance and driver package using benchmarking and geometry analysis.
- Estimate subsystem masses and static axle loads.
- Estimate centre-of-gravity position and height with uncertainty noted.
- Package driver, controls, brakes, motor, battery, controller, axle, chain and guards.
- Calculate preliminary road loads and assess 60 and 80 km/h feasibility.

**Outputs:** dimensioned layout, mass budget, packaging model, first-pass performance model.

### Phase 4 — Mechanical subsystem design (Weeks 3–5)

**Chassis**
- Define load paths, candidate material/sections, joints, weld access, mounts and inspection access.
- Evaluate torsional stiffness, bending, local buckling, fatigue-sensitive details and impact-related load cases.
- Define datums and repeatable fabrication/fixture strategy.

**Steering and front assembly**
- Define steering axis, steering arms, linkage, Ackermann intent, turning radius, stops, scrub radius and clearances.
- Size spindles, hubs, bearings, fasteners and supports for combined loads.

**Rear axle and drivetrain**
- Define axle support, bearing span, sprocket position, chain line, adjustment, guarding and hubs.
- Calculate axle torque/bending, bearing reactions, chain tension and gear ratio.

**Brakes**
- Define deceleration and stopping-distance requirements.
- Calculate brake torque and assess disc/caliper/master-cylinder compatibility, mount loads, thermal duty and serviceability.

**Outputs:** subsystem CAD, calculations, drawings, interface checks.

### Phase 5 — Electric powertrain and battery (Weeks 5–6)

**Motor and controller**
- Derive wheel tractive force/torque from vehicle mass, acceleration, road loads and grade.
- Select motor from continuous and peak duty, torque-speed curve, thermal limits and controller compatibility.
- Calculate gearing using loaded tyre radius and motor speed limits.
- Check current limits, cooling, brake/throttle logic and fault behaviour.

**Battery and electrical**
- Derive usable energy from range and duty-cycle demand.
- Calculate continuous/peak current, voltage sag, cell limits, conductor sizing, losses and thermal conditions.
- Select cells, BMS, fuse, contactor, precharge if required, isolation, connectors, enclosure and monitoring.
- Document polarity, routing, strain relief, abrasion protection, segregation and emergency shutdown.
- Obtain competent review of battery design and high-current electrical work.

**Outputs:** sizing workbook, component datasheets, electrical block diagram, wiring schematic, battery packaging CAD, hazard review.

### Phase 6 — Engineering calculations (Weeks 6–7)

Maintain traceable calculations with inputs, units, sources, assumptions, equations, outputs and revision.

- Road loads: aerodynamic drag, rolling resistance and grade.
- Performance: wheel force, wheel/motor torque, power, gearing, speed and acceleration.
- Energy: duty-cycle energy, usable capacity, current, losses and range.
- Dynamics: axle loads, load transfer and turning geometry.
- Braking: brake force, torque, stopping distance and thermal duty.
- Structures: chassis members, axle torsion/bending, spindle stress, bearings, fasteners and weld/joint assumptions.
- Electrical/thermal: voltage drop, cable ampacity, protection coordination and component operating limits.

**Output:** calculation package and independent checks of critical results.

### Phase 7 — CAD development and integration (Weeks 6–9)
- Use master layout sketches and a documented coordinate/datum strategy.
- Build parametric parts and subsystem assemblies.
- Integrate using controlled interfaces.
- Check steering travel, wheel/tyre clearances, chain line/guard, brake clearance, service access, driver egress, cable routing and battery removal.
- Compare CAD mass properties against the mass budget.
- Maintain native CAD and neutral exports; release drawings under revision control.

**Outputs:** integrated native assembly, neutral model, drawings, mass and interference reports.

### Phase 8 — Simulation and verification (Week 10)

**ANSYS**
- Static structural analysis for justified load cases.
- Modal analysis where relevant.
- Axle, spindle and mounting analyses.
- Document material data, contacts, constraints, loads, mesh quality, convergence/sensitivity and limitations.

**MATLAB/Simulink**
- Longitudinal vehicle model with road loads and drivetrain efficiency.
- Motor torque-speed/controller limits.
- Gear-ratio sweep.
- Battery energy/current model.
- Braking and range estimates.

Compare hand calculations and numerical models with simulations; investigate discrepancies. FEA plots alone do not prove safety.

**Outputs:** verification matrix, models, reports and design actions.

### Phase 9 — Design freeze and manufacturing package (Week 11)
- Close critical design-review actions.
- Freeze interfaces, geometry, materials and component selections.
- Produce released part/assembly drawings, tube cut list, weld details, tolerances, fastener schedule and inspection criteria.
- Prepare BOM with supplier, part number, quantity, quote date, lead time and cost status.
- Include assembly sequence, tooling/fixture requirements, quality checks and rework criteria.
- Reconcile quoted cost with the budget and retain contingency.

**Outputs:** released manufacturing package and costed BOM.

### Phase 10 — Fabrication, commissioning and testing (Week 12 planning; physical work follows)
- Inspect incoming materials and components.
- Fabricate to approved drawings using qualified processes.
- Inspect welds, alignment, fasteners, steering, brakes, chain guard, battery retention and cable routing.
- Commission electrical systems using safe isolation and current-limited procedures.
- Complete static checks and low-speed shakedown before progressive expansion of the test envelope.
- Test only in a controlled closed area with competent supervision, suitable PPE and a documented abort plan.
- Record vehicle configuration, test personnel, conditions, instrumentation, raw data, results and corrective actions.

**Outputs:** inspection records, test plan, data and validation report.

## 4. Twelve-week design schedule

| Week | Focus | Milestone |
|---|---|---|
| 1 | Research and benchmarking | Benchmark matrix |
| 2 | Requirements, architecture, preliminary layout | Requirements/concept review |
| 3 | Chassis concept and load paths | Chassis concept review |
| 4 | Steering and front assembly | Front-end review |
| 5 | Rear axle, drivetrain and brakes | Mechanical review |
| 6 | Motor, controller, battery and electrical architecture | Powertrain review |
| 7 | Consolidated calculations | Calculation review |
| 8 | CAD integration | Integration review |
| 9 | CAD completion and drawings | CAD review |
| 10 | ANSYS and MATLAB/Simulink verification | Analysis review |
| 11 | BOM and manufacturing package | Cost/design release review |
| 12 | Final documentation and validation plan | Design release |

This is a planning baseline. Fabrication, procurement and physical testing may require additional time.

## 5. Final deliverables

1. Requirements and verification register.
2. Benchmarking and source register.
3. Vehicle architecture and interface-control document.
4. Mass budget and packaging layout.
5. Subsystem CAD and complete assembly.
6. Engineering calculation workbook/scripts.
7. ANSYS and MATLAB/Simulink models and reports.
8. Electrical architecture and wiring documentation.
9. Manufacturing drawings and inspection plan.
10. Costed BOM and procurement status.
11. Risk register and validation/test plan.
12. Final technical report.

## 6. Definition of design completion

All critical requirements have verification paths; subsystem interfaces are closed; the full CAD package is integrated; critical calculations and simulations are reviewed; the BOM is costed; manufacturing documents are released; and safety and validation actions are documented.
