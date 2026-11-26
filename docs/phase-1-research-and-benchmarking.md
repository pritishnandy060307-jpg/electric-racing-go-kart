# Phase 1 — Research and Benchmarking

**Status:** Not started  
**Purpose:** Build an evidence-based understanding of existing electric racing go-karts before freezing requirements or beginning detailed CAD.

> **Rule:** Do not select dimensions or components because they look reasonable. Record the source, units, operating context, and confidence for every value. If a manufacturer does not publish a value, write **Not published** rather than guessing.

## Phase 1 task checklist

### 1. Study existing electric racing go-karts

- [ ] Understand the main electric kart categories:
  - [ ] Competitive/sprint racing karts
  - [ ] Endurance-oriented racing karts
  - [ ] Commercial/rental electric karts
- [ ] Understand how these categories differ in mass, power, speed, duty cycle, cooling, battery capacity, chassis construction, and serviceability.
- [ ] Identify at least **5 relevant electric kart models**. Prioritise models with manufacturer documentation and technical specifications.
- [ ] For each model, record the manufacturer, exact model name, intended use, source links, and date accessed.
- [ ] Separate true electric racing karts from rental/fleet karts. Keep rental models as secondary references unless their design is directly relevant.
- [ ] Prepare a short note describing which design features appear relevant to this project's endurance-focused, rear-wheel-drive kart.

**Deliverable:** **research/electric-kart-study.md** with model list, category notes, source links, and key observations.

### 2. Build the kart benchmarking matrix

- [ ] Create a comparison table for the selected models.
- [ ] Collect the following where published:
  - [ ] Overall length, width, height, and wheelbase
  - [ ] Front and rear track widths
  - [ ] Vehicle mass (state whether battery is included)
  - [ ] Tyre dimensions and wheel diameter
  - [ ] Chassis material, construction, and adjustment features
  - [ ] Motor type, rated/continuous power, peak power, and voltage
  - [ ] Controller/inverter details, if available
  - [ ] Battery chemistry, nominal voltage, capacity (Ah and kWh), and mass
  - [ ] Drive arrangement and transmission/final-drive details
  - [ ] Brake arrangement
  - [ ] Published maximum speed, range, or endurance duration
  - [ ] Charging time and cooling approach, if published
- [ ] Mark every unavailable item as **Not published**.
- [ ] Do not mix peak and continuous power, nominal and maximum voltage, or vehicle mass with and without the battery.
- [ ] Add a source URL and a short source note for every specification.

**Deliverable:** **research/kart-benchmark-matrix.csv** (or an equivalent spreadsheet).

### 3. Research the major subsystems

- [ ] **Chassis:** tubular frame layouts, material grades, tube sizes, joints, torsional stiffness, and repairability.
- [ ] **Powertrain:** BLDC/PMSM options, motor speed-torque curves, continuous versus peak ratings, controller compatibility, and cooling.
- [ ] **Battery:** cell formats and chemistry, pack voltage, energy, discharge capability, BMS, enclosure, isolation, and serviceability.
- [ ] **Drivetrain:** rear axle, bearings, hubs, sprockets, chain, reduction ratio, and alignment.
- [ ] **Tyres and wheels:** available kart tyre sizes, loaded rolling radius, grip, wear, and pressure requirements.
- [ ] **Braking:** disc/caliper/master-cylinder arrangements, stopping performance, and independent safety considerations.
- [ ] **Steering and ergonomics:** steering geometry, steering components, seat position, pedal reach, and driver packaging.

**Deliverable:** A source-backed subsystem research note and a shortlist of candidate components. No purchase or final selection at this stage.

### 4. Build the source and assumptions register

- [ ] Create **research/source-register.md**.
- [ ] Record title, organisation/manufacturer, URL, publication date (if known), access date, and what information the source supports.
- [ ] Classify each value as **manufacturer-published**, **supplier-published**, **measured**, **estimated**, or **calculated**.
- [ ] Record conflicting specifications instead of silently choosing one.
- [ ] Keep assumptions separate from verified facts.

**Deliverable:** A traceable source register.

### 5. Write the benchmarking conclusions

- [ ] Identify the most relevant reference kart(s) and explain why they are comparable.
- [ ] Summarise observed ranges for mass, wheelbase, track, tyre size, motor power, battery energy, and speed where sufficient data exists.
- [ ] Explain which specifications are missing and what must be measured or derived independently.
- [ ] List the major design questions that remain open.
- [ ] Recommend the next engineering calculations required before the requirements and architecture are frozen.

**Deliverable:** **research/phase-1-benchmarking-summary.md**.

## Suggested order and timebox

| Work block | Suggested time | Exit condition |
|---|---:|---|
| Task 1 — Understand electric kart types and identify models | 1 day | At least 5 relevant models identified and categorised |
| Task 2 — Collect comparable specifications | 1–2 days | Benchmark matrix populated with sources and explicit gaps |
| Task 3 — Subsystem research | 2 days | Source-backed notes for all major subsystems |
| Task 4 — Source register | Alongside research | Every important value is traceable |
| Task 5 — Conclusions | 0.5–1 day | Benchmarking summary and open questions written |

The timebox is a planning estimate, not a reason to fill gaps with guesses.

## Phase 1 completion criteria

Phase 1 is complete only when:

- [ ] At least five relevant electric kart models have been studied.
- [ ] The benchmark matrix distinguishes competitive racing and rental/fleet references.
- [ ] Important published specifications have source links and consistent units.
- [ ] Missing information is explicitly marked; no invented specifications remain.
- [ ] Major subsystem research notes are available.
- [ ] A concise benchmarking summary identifies the next calculations and decisions.

## Important boundary

**Do not begin detailed chassis fabrication design or buy major components during Phase 1.** The purpose is to learn the design space and gather evidence. Requirements, geometry, motor, controller, battery, gearing, brakes, and chassis dimensions must be selected in later phases using calculations, compatibility checks, safety review, and budget verification.
