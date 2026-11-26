# Vehicle Geometry and Packaging — Design Baseline V0.1

**Status:** Preliminary method and parameter register; no geometry is released for fabrication.  
**Vehicle:** Single-seat, rear-wheel-drive electric racing go-kart  
**Driver design mass:** 85 kg  
**Performance intent:** 60–80 km/h maximum-speed target; 20 km range target  
**Budget target:** ₹40,000–₹60,000

## 1. Purpose and design rule

This document defines how the vehicle's principal dimensions and component locations will be established. It is not a final dimensioned design. Wheelbase, track width, tyre size, ground clearance and component coordinates must be selected from a benchmark study, supplier data, packaging checks and calculations—not copied from an arbitrary kart or guessed to make the CAD assembly look plausible.

Maintain a parameter table and record the source, rationale, revision and verification status for every released value.

## 2. Coordinate system and datums

Use a vehicle-fixed right-handed coordinate system for all sketches, CAD parts, calculations and simulation:

- **X:** longitudinal, positive forward.
- **Y:** lateral, positive to the vehicle's left.
- **Z:** vertical, positive upward.
- **Origin:** ground-plane projection of the rear axle centreline at vehicle centreline, with the kart at nominal static ride condition.

Define and retain these datums in the master layout:
- Rear axle centreline: X = 0.
- Vehicle centreplane: Y = 0.
- Ground reference plane: Z = 0.
- Front axle centreline: X = wheelbase (L).

Use millimetres in CAD drawings and SI units in calculations. State whether dimensions refer to tyre outer surfaces, wheel centre planes, chassis tubes or component mounting faces.

## 3. Geometry parameter register

| Parameter | Symbol | Current status | How to determine |
|---|---|---|---|
| Wheelbase | L | Open | Benchmark comparable karts; evaluate stability, turning and packaging |
| Front track | Tf | Open | Tyre envelope, steering geometry, lateral stability and rules/venue constraints |
| Rear track | Tr | Open | Rear tyre envelope, axle/hub layout and stability |
| Loaded tyre radius | Rw | 0.13 m preliminary calculation assumption only | Select tyre/wheel and measure loaded radius |
| Tyre width and diameter | Wt, Dt | Open | Supplier data and physical measurement |
| Ground clearance | Hgc | Open | Surface, chassis low points, tyre deflection and operating environment |
| Seat reference point | Xs, Zs | Open | Driver fit, pedal reach, steering reach, visibility and egress |
| Battery envelope/location | Xb, Yb, Zb | Open | Selected pack dimensions, retention, protection, cooling and service access |
| Motor location | Xm, Ym, Zm | Open | Chain line, sprocket clearance, cooling, mount loads and service access |
| Axle/bearing locations | Xa, Xbr | Open | Axle bending, bearing reactions, sprocket and brake-disc positions |
| CG location | Xcg, Ycg, Zcg | Open | Component mass properties and later physical measurement |

**Important:** The 0.13 m loaded wheel radius is only the placeholder used in the first-pass performance workbook. It is not a selected tyre specification.

## 4. Packaging sequence

Complete packaging in this order so that downstream geometry is based on real interfaces:

1. **Tyres and wheels:** shortlist commercially available kart tyres/wheels; record overall diameter, section width, rim, pressure range, load/speed suitability and loaded radius.
2. **Driver package:** model the 85 kg design driver using an adjustable reference manikin or measured anthropometric envelope. Define seat back angle, hip point, pedal reach, steering-wheel reach, knee/foot clearance, visibility and emergency egress.
3. **Axle and rear assembly:** place axle, bearings, hubs, rear wheels, sprocket, brake disc and caliper. Check bearing span, chain line, chain adjustment and rotating-part guard.
4. **Front assembly:** place front wheels, hubs, kingpins/spindles, steering arms, tie rods, steering column and stops. Check full-lock tyre/chassis/pedal interference.
5. **Powertrain:** package motor and controller using actual datasheet dimensions, mass, mounting faces, cable bend radii and cooling requirements.
6. **Battery:** package the complete enclosure, not just the cells. Include BMS, fuse, contactor, isolation/service access, connectors, cable exits, retention and protective structure.
7. **Chassis:** connect the hard points with plausible load paths; ensure weld/tool access, inspection access and manufacturable joints.
8. **Guards and service:** add chain/sprocket guards, electrical protection, access panels and removal paths before declaring packaging complete.

## 5. First-order geometry checks

### 5.1 Static axle loads

Let:
- m = total vehicle-plus-driver mass,
- L = wheelbase,
- xcg = longitudinal CG position measured forward from the rear axle,
- g = 9.81 m/s².

For a level surface and static equilibrium:

- Front axle load: Fz,f = m g (xcg / L)
- Rear axle load: Fz,r = m g (1 - xcg / L)

Check that both loads are positive and that wheel, tyre, axle, bearing, spindle and brake components are rated for the resulting loads with appropriate dynamic margins. Recalculate after every major component relocation.

### 5.2 Lateral stability screening

For a simplified rigid vehicle on a level surface, a first-order geometric rollover screening estimate is:

- a_y,tip / g ≈ (track / 2) / hcg

where track is the relevant support width and hcg is CG height above the ground. This is not a safe cornering limit: tyre grip, suspension/chassis compliance, transient load transfer, uneven surfaces, driver movement and inside-wheel lift behaviour also matter. Use the estimate only to compare early layouts, then perform a more complete dynamics assessment.

### 5.3 Steering and turning

The front steering layout must be checked at straight-ahead and both steering-lock extremes. Establish:
- Steering-axis and steering-arm geometry.
- Ackermann intent and inner/outer wheel angles.
- Minimum turning radius from the actual wheelbase and steering angles.
- Mechanical steering stops.
- Tyre-to-chassis, tyre-to-pedal, tie-rod and brake-hose clearances.
- No binding or over-centre linkage condition through the full travel.

Do not set steering angles from a single generic rule. Derive them from the intended turning behaviour and verify the actual linkage in CAD.

### 5.4 Ground and component clearances

Check tyre clearance at full steering lock, chain and sprocket clearance through adjustment range, brake-disc/caliper clearance, battery enclosure clearance from the ground, and clearance to all chassis members. Include tyre growth/deflection, manufacturing tolerances, fastener heads, cable routing and guard thickness.

## 6. Centre-of-gravity workflow

1. Assign realistic mass and centre-of-mass properties to every component from datasheets, CAD or measured mass.
2. Include the driver in the seated design position.
3. Calculate the combined CG from component mass moments:
   - Xcg = Σ(mi xi) / Σmi
   - Ycg = Σ(mi yi) / Σmi
   - Zcg = Σ(mi zi) / Σmi
4. Check static axle loads against the axle-load equations above.
5. Run sensitivity cases for uncertain battery, chassis and driver positions.
6. After fabrication, estimate CG and axle loads by a controlled weighing method and compare against the model.

A CAD mass-property result is only as good as its assigned material densities, component masses and driver model.

## 7. SOLIDWORKS implementation

Create a master layout part or skeleton assembly containing:
- Ground plane and vehicle centreplane.
- Front and rear axle centre planes.
- Wheel/tyre envelope cylinders.
- Seat reference point and driver envelope.
- Steering column, spindle and steering-linkage hard points.
- Motor, battery enclosure, controller, brake and axle envelopes.
- Chain centreline and adjustment envelope.
- Chassis keep-out and ground-clearance planes.

Use global variables/equations for wheelbase, front/rear track, tyre diameter, tyre width and key component coordinates. Link subsystem parts to stable master datums rather than face-to-face references where practical. Keep a configuration or revision for each geometry review.

Export a top, side and front layout drawing with dimensions, datum references, mass properties and unresolved clashes.

## 8. Required CAD and analysis reviews

Before geometry is accepted, complete the following:

- [ ] Driver can enter/exit and reach pedals and steering without interference.
- [ ] Seat and driver position are compatible with visibility and control operation.
- [ ] Front tyres clear chassis, pedals and steering components at both steering locks.
- [ ] Rear tyres clear chassis, axle hardware and guards.
- [ ] Chain alignment and adjustment are achievable; chain and sprockets are guarded.
- [ ] Brake disc, caliper, pedal and hydraulic routing fit and remain serviceable.
- [ ] Battery enclosure is retained, protected and removable for service.
- [ ] Motor/controller cooling and cable routing are credible.
- [ ] Static axle loads and component load ratings are checked.
- [ ] CG estimates and uncertainty/sensitivity cases are documented.
- [ ] Ground clearance is checked at all low points.
- [ ] No unresolved interference, inaccessible fastener or impossible assembly sequence remains.
- [ ] Geometry is checked against applicable competition/venue rules, if relevant.

## 9. Design decisions still open

Do not freeze the following until supporting evidence is available:
- Tyre and wheel size.
- Wheelbase and front/rear track.
- Ground clearance.
- Seat and pedal geometry.
- Steering layout and steering stops.
- Battery enclosure dimensions and location.
- Motor position, sprocket sizes and chain line.
- Axle/bearing arrangement.
- Chassis tube layout and section sizes.

Record each decision in `docs/design-decisions/` with alternatives, evidence, calculations, consequences and approval status.

## 10. Exit criteria

The geometry-and-packaging stage is complete only when:
1. The tyre/wheel and major component envelopes are based on identified candidate parts.
2. Driver ergonomics and egress have been checked.
3. A dimensioned master layout exists in top, side and front views.
4. Steering, chain, brake and service clearances are checked.
5. Static axle loads and CG estimates are documented with assumptions.
6. Major interfaces and unresolved risks are recorded.
7. The layout has passed a design review and is clearly marked preliminary or released.

No dimensions in this document constitute fabrication approval.
