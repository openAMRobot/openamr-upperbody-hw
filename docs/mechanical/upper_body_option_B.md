# Upper-body mounting, option B

> **Status:** Decided design values, not a released design. Decision of record: P-03 revision 18.9 item 18, 9 October 2026 ("option B"). Supplier CAD items marked *pending* below are not yet available; nothing in this page is a fabrication release, a stability result or a safety claim.

## Coordinate convention

All heights are measured from the floor, Z = 0. Axes follow REP 103: x forward, y left, z up. The column axis is the vertical axis of the lift column; fore-aft positions are given relative to it.

## Decided values

| Item | Value |
|---|---|
| Lift column | DOLD Hexalift V4, 350 mm stroke |
| Column length | 530 mm retracted, 880 mm extended |
| Column orientation | Mounted with its 240 mm side fore-aft |
| Base plate | 10 mm aluminium on the 294 mm chassis deck; top face 304 mm |
| Base-plate positions | Two fore-aft positions only: `bp000` (centre, the existing mast position) and `bp050` (+50 mm forward) |
| Arm profile | MISUMI HFS6-60120 (60 mm lateral, 120 mm fore-aft), 340 mm long |
| Arm profile support | Stands on a 10 mm adapter plate on the column top, 120 mm ahead of the column front face |
| Arm profile span | 844 to 1184 mm at the retracted lift |
| Arm mount point | OpenArm J1_A, frame `openarm_{side}_base_link`: x = column axis + 180 mm, y = ±31 mm, roll, pitch and yaw 0 |
| Shoulder height | 1000 mm at lift 0, 1350 mm at lift 350 mm (at the arm mount point) |
| Lift joint | Prismatic, 0 to 350 mm; the lift height is joint state |
| Lift calibration stops | `L1000`, `L1175`, `L1350` (calibration IDs, not configuration IDs) |
| Head camera | Stereolabs ZED Mini on the lift carriage; lens 22 mm ahead of and 223 mm above the arm mount point, centred at y = 0 |
| Head-camera pitch | 15 to 35 degrees down in 5 degree steps, IDs `hp15` to `hp35`, baseline `hp25` |
| Maximum assembled height | 1700 mm |

The upstream OpenArm body (`openarm_body_link0`) is not used.

## Configuration IDs

| Configuration axis | IDs |
|---|---|
| `column` | `dold_v4_350`, `tl3_400` |
| `base_plate` | `bp000`, `bp050` |
| `head_pitch` | `hp15`, `hp20`, `hp25` (baseline), `hp30`, `hp35` |
| `base_tilt` | `bt05`, `bt10`, `bt15` |

Each configuration ID must propagate to URDF/Xacro, TF, SRDF/MoveIt, camera calibration, the configuration hash and dataset metadata (owned by `openamr-upperbody-sw` and the interface contracts). The lift stops `L1000`, `L1175` and `L1350` are calibration IDs; the current lift height is published as joint state, not as a configuration ID. No column lengths for `tl3_400` are recorded here; they are pending supplier data.

## Height stack

| Level | Retracted lift (mm) | Extended lift (mm) |
|---|---|---|
| Floor | 0 | 0 |
| Chassis deck top | 294 | 294 |
| Base-plate top face (height reference) | 304 | 304 |
| Column top (304 + column length) | 834 | 1184 |
| Adapter-plate top, arm profile bottom (+10) | 844 | 1194 |
| Arm mount point, shoulder (304 + column length + 166) | **1000** | **1350** |
| Arm profile top (+340 from profile bottom) | 1184 | 1534 |
| Head-camera lens (shoulder + 223) | 1223 | 1573 |

Shoulder height = 304 + 530 + 166 = 1000 mm retracted, and 304 + 880 + 166 = 1350 mm extended. The 1700 mm maximum assembled height applies to the complete robot, including the head camera and its bracket, at full lift extension. The lens line is at 1573 mm; the height of the camera body and bracket above the lens line comes from supplier CAD and is pending.

## Fore-aft layout

| Item | x relative to the column axis |
|---|---|
| Column axis, `bp000` | 0 (the existing mast position) |
| Column axis, `bp050` | +50 mm relative to `bp000` |
| Arm mount point (J1_A, `openarm_{side}_base_link`) | +180 mm |
| Head-camera lens | +202 mm (arm mount point + 22 mm) |

With the column's 240 mm side fore-aft, the column front face lies 120 mm ahead of the column axis if the axis is at the column centre. That centring is an assumption pending the DOLD CAD.

## Fastening

### Lift column to base plate

- 4 × M8 DIN 7500 thread-forming countersunk screws, inserted from below and seated flush with the underside of the base plate.
- At least 20 mm thread engagement in the column foot.
- The DOLD hole pattern is from supplier CAD, *pending*.

### Base plate to chassis deck

- 4 × M8 on the 190 × 300 mm pattern.
- The 10 mm base plate is not tapped.
- The orientation of the deck pattern (which side runs fore-aft) is from supplier CAD, *pending*.

## Head-camera bracket

- The supplied OpenArm camera mount holds the ZED Mini at its ends.
- The pitch bracket pivots on the lens line, so the lens position (22 mm ahead of and 223 mm above the arm mount point) does not change between `hp15` and `hp35`.

## Pending from supplier CAD

| Item | Source | Status |
|---|---|---|
| DOLD Hexalift V4 hole patterns (foot and top plate) | DOLD CAD | From supplier CAD, pending |
| OpenArm J1_A plate outline | OpenArm CAD | From supplier CAD, pending |
| Chassis deck 190 × 300 mm pattern orientation | Chassis CAD | From supplier CAD, pending |
| Column centring relative to its 240 mm side | DOLD CAD | From supplier CAD, pending |
| Camera body and bracket height above the lens line | Stereolabs and OpenArm CAD | From supplier CAD, pending |
| TiMOTION TL3 400 (`tl3_400`) retracted and extended lengths | TiMOTION data | Pending |

## Not covered here

Lift holding on E-stop and power loss, the lift driver and its interface, motion interlocks and the stability (F2S) rerun for both base-plate positions are separate release gates owned elsewhere. This page does not implement or validate any of them.
