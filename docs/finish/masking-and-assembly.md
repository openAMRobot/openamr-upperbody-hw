# Masking and assembly sequence, upper body

Order of work for the 2.0 prototype upper body. Plates are anodised before any part is fitted;
purchased parts are never coated and are protected while other work goes on near them. The mobile base
sequence (openamr-platform-hw `docs/finish/masking-and-assembly.md`) ends with the coated cover, its
lift base plate footprint left bare.

## 1. Plates (before assembly)

| Part | Before anodising | Process |
|---|---|---|
| Lift base plate (10 mm 6082-T6) | machine all holes and countersinks per the drawing (pending); mark the bonding point | black anodise; bonding point masked with an anodising plug or spot-faced to bare metal afterwards |
| Adapter plate (10 mm 6082-T6, 360 x 100 mm) | machine all holes; mark the bonding point | black anodise; bonding point as above |
| Rear upright with stiffener (MEC-004) | machine; material to be confirmed | black anodise if aluminium; RAL 9005 matte powder with T-nut faces masked if steel |
| Head camera pitch bracket (ARM-011, own bracket only if the supplied mount does not fit) | pivot bore and pitch index holes defined | black filament if printed; RAL 9005 matte powder with the pivot bore and index holes masked if steel; black anodise if aluminium |

Anodising leaves a thin hard layer (typically 10 to 25 micrometres) on the clamped faces; the joint
owner confirms it is acceptable (feasibility list). Threads are not anodised after tapping unless plugged.

## 2. Purchased parts (no finishing)

- Arm profile: ordered with the dark anodised finish if offered, otherwise as delivered. Never painted,
  wrapped or taped in the slots.
- DOLD Hexalift V4: as delivered. Keep the telescoping sections and seals covered with a loose clean
  sleeve while working above; never tape them.
- OpenArm 2.0 kit, ZED Mini, supplied camera mount, chest E-stop: as delivered.

## 3. Assembly order and protection

1. Check the cover footprint on the mobile base is bare and clean; fit the lift base plate with four
   M8 on the 190 x 300 mm pattern (bp000 or bp050). Connect and measure the bonding point.
2. Fit the DOLD column to the base plate with 4 x M8 DIN 7500 from below. Sleeve the column.
3. Fit the adapter plate on the column top, then the arm profile from below into its end-tapped core
   holes, then the rear upright with T-nuts in the two rear slots.
4. Fit the OpenArm J1_A plates on the side T-slots (y +/-31 mm, one 1 mm spacer each) and the arms.
   Keep cables and labels uncovered.
5. Route the mast cables and fit the cable guards (MEC-013); record which slots the route uses.
6. Fit the chest E-stop where the CAD places it. Record its position for keep-out K1.
7. Fit the head camera pitch bracket on the profile top and the ZED Mini in its supplied mount. Keep
   the lens caps on until calibration.
8. Last, and only after steps 4 to 6 confirm the slots are free: push in slot strips I1 and I2. They
   come out by hand for any later change.
9. I3 (OpenArm printed inserts), only once identified: swap the delivered printed part for the orange
   reprint, keeping the delivered part as the spare.
10. Remove the column sleeve and the lens caps.

## 4. Final checks on the upper body

- Column telescoping surfaces clean, no added parts or film; full stroke runs free.
- No coating in the T-slots or core holes; T-nuts slide.
- Bonding points bare and connected (resistance value set by the electrical owner).
- Chest E-stop red on yellow; no orange or cyan within 150 mm (K1).
- I1 and I2 leave three slots free on each side face and both front slots free.
- Head camera lenses and OpenArm in-hand camera windows clear.
- No adhesive on any functional surface; no new holes.
