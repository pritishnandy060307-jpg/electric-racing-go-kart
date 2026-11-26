# Vehicle Architecture — Initial Concept

## 1. System overview

Proposed single-seat electric go-kart with rear-wheel propulsion. This architecture is preliminary and will be revised after requirements, packaging, performance sizing, safety analysis and supplier review.

## 2. Mechanical power flow

Driver throttle request → motor controller → electric motor → drive sprocket → chain → axle sprocket → rear axle / driven wheels.

Account for torque reaction, chain tension, alignment, adjustment, rotating-part guarding, bearing support and service access.

## 3. Electrical energy and control flow

Battery pack → main fuse / isolation and contactor architecture → motor controller → motor.

The low-voltage control and monitoring design must define:
- Driver throttle input and fault handling.
- Brake input and propulsion-inhibit strategy.
- Driver-accessible emergency shutdown.
- Battery and controller monitoring.
- Safe power-up, shutdown and fault response.
- Precharge if required by selected equipment.

Exact topology and ratings are not selected yet. They require datasheets, calculations and qualified review.

## 4. Subsystems and interfaces

| Subsystem | Main interfaces | Design evidence |
|---|---|---|
| Chassis | Seat, steering, front supports, axle bearings, motor/battery mounts, brake mounts | Loads, drawings, structural analysis |
| Driver package | Seat, restraint, pedals, controls, egress | Ergonomic and safety review |
| Steering/front | Column, linkage, spindles, hubs, wheels | Geometry, loads, clearance |
| Rear axle | Bearings, hubs, sprocket, wheels, brake disc | Torque, bending, bearing and alignment checks |
| Brakes | Pedal, master cylinder, lines, caliper, disc, mount | Torque, stopping and thermal calculations |
| Motor/controller | Mount, chain line, cooling, electrical and control interfaces | Torque-speed and thermal compatibility |
| Battery | Enclosure, mounts, BMS, fuse, contactor, service isolation | Energy/current/thermal and hazard review |
| Tyres/wheels | Hubs, bearings and vehicle loads | Load/speed compatibility |
| Instrumentation | Sensors, display/logging, wiring | Measurement and electrical interface specification |

## 5. Packaging principles

- Keep mass low and secure; assess centre-of-gravity effects.
- Preserve driver space, pedal travel, visibility and safe egress.
- Maintain access to serviceable components and isolation devices.
- Guard chain, sprockets and other rotating components.
- Protect wiring from heat, abrasion, pinch points and moving parts.
- Mechanically protect the battery enclosure and allow inspection.
- Maintain wheel, tyre, steering, brake and chassis clearances through full operating travel.

## 6. Open architecture decisions

- Motor type, voltage, continuous/peak rating and cooling.
- Battery chemistry, cell configuration, usable energy, BMS and protection.
- Axle type, diameter, bearing layout and sprocket arrangement.
- Wheel/tyre size and load/speed rating.
- Chassis geometry, tube sections, materials and fabrication process.
- Brake architecture.
- Vehicle mass, wheelbase, track, centre of gravity and driver package.

Record decisions and evidence in `docs/design-decisions/`.
