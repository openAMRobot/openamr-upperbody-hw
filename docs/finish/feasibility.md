# Feasibility list, upper body

Each item is in one category. An item leaves the list when its check is recorded (drawing revision,
measurement or written confirmation) in the PR that changes its status in `finishes.yaml`.

## Now (sources establish material and process)

| Item | Why it can proceed |
|---|---|
| DOLD Hexalift V4 as delivered, no inserts or paint | purchased telescoping column; no operation |
| OpenArm 2.0 metal parts, actuators and grippers as delivered | purchased kit; no operation |
| ZED Mini and supplied camera mount as delivered | purchased; no operation |
| No strips on the rear face or the front face of the profile | rear slots carry the rear upright T-nuts; front slots kept free |
| finishes.yaml read by the model | ids unique across both files; checked by `tools/finish_tables.py --companion` |

## Needs CAD or drawing confirmation

| Item | Exact check needed |
|---|---|
| Lift base plate finish and bonding point | lift base plate drawing (outline, holes, bonding point; pending) |
| Adapter plate and rear upright | MEC-004 drawing (outline, holes, material of the rear upright, bonding point) |
| I1 and I2 position and length | OpenArm J1_A plate outline and which side slots it uses (OpenArm CAD pending); mast cable route; strip length from the adapter plate to the J1_A plate (about 85 mm in the preview) |
| Chest E-stop position | CAD position on the mast, to apply keep-out K1 to I1, I2 and I3 |
| Head camera bracket | design and material (ARM-011; supplied mount fit check first) |
| Column outline for the model | DOLD CAD (lateral width, centring relative to the 240 mm side, hole patterns) |
| Mast cable guards (MEC-013) | cable route and part list |

## Needs supplier confirmation

| Item | Confirmation |
|---|---|
| Dark anodised HFS6-60120 | manufacturer confirms a black or graphite anodised finish for this section at 340 mm with both ends tapped; otherwise the profile stays as delivered |
| HFS6-60120 slot layout | MISUMI outline drawing: slot count and positions on the 60 and 120 mm faces (assumed 2 and 4) |
| Cyan slot cover strip | a 6 series 8 mm slot cover offered in a colour close to RAL 5018; otherwise a printed TPU strip |
| Black anodise of 6082-T6 plates | anodiser confirms colour and masking of bonding points |
| OpenArm 2.0 printed parts (I3) | Enactic 2.0 BOM or CAD: which parts are printed, their material, whether structural; files under CERN-OHL-S-2.0 |

## Needs a fit check

| Item | Fit check |
|---|---|
| I1, I2 in the anodised slot | push-in by hand, holds without adhesive, at most 1 mm proud, clears the J1_A plate and spacer, removable by hand |
| I3 reprint | fit, function and strength equal to the delivered part; gripper and camera field of view unchanged |
| Anodised plates in the bolted joints | lift base plate on the cover, column foot, adapter plate seat: torque and bonding resistance measured |
| Colour sample | RAL 5018 strip and RAL 2004 filament sample against the RAL 7016 cover coupon, the profile sample and the OpenArm parts in daylight; cyan reference checked against a physical RAL 5018 sample |
