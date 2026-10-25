# Insert and trim schedule, upper body

An insert or trim is any part added only for appearance. The plan keeps them few, light and removable,
with no new holes and no adhesive on functional surfaces. There are three inserts on the whole robot,
all on the upper body; the mobile base has none.

## Arm profile slot use

The arm profile is a MISUMI HFS6-60120 (6 series, 8 mm slot), 340 mm long, standing on the adapter
plate with its 120 mm side fore-aft and its 60 mm side lateral (option B page). Slot count and positions
are **assumed** from the 30 mm grid of the 6 series and from the BOM wording "T-nuts in the two rear
slots": two slots on each 60 mm face and four on each 120 mm face, at 15 and 45 mm either side of the
face centre. Verify against the MISUMI outline drawing before ordering strips.

| Face | Width | Slots (assumed) | Use stated by the sources | Strip | Kept free |
|---|---|---|---|---|---|
| Left (+y) | 120 mm | 4 | left OpenArm J1_A plate on the side T-slots, y +31 mm with a 1 mm spacer (BOM rows MEC-003, ARM-001; plate outline pending) | **I1**: front-most slot, lower segment only | the other three slots, and the front-most slot above the J1_A plate |
| Right (-y) | 120 mm | 4 | right J1_A plate, y -31 mm | **I2**: front-most slot, lower segment only | the other three slots, and the front-most slot above the J1_A plate |
| Front (+x) | 60 mm | 2 | none stated; chest E-stop position and mast cable route unknown | none | both, for later mounting |
| Rear (-x) | 60 mm | 2 | rear upright with stiffener, T-nuts in both rear slots (BOM row MEC-003) | none | none free at the upright height; both slots are fastening slots |
| Bottom end | 60 x 120 mm | end-tapped core holes | bolted from below through the adapter plate (BOM row MEC-004) | none | not applicable |
| Top end | 60 x 120 mm | end-tapped core holes | head camera pitch bracket on the profile top (BOM row ARM-011) | none | not applicable |

Wiring and heat: the BOM says the mast carries "arms, head camera, chest E-stop and cable routing";
the cable route on the profile is not drawn. A strip goes in only where the CAD shows the slot is not
used for fastening, adjustment, wiring or heat.

## Inserts

### I1 and I2, slot cover strips (cyan)

| Field | I1 | I2 |
|---|---|---|
| Location | left (+y) face, front-most slot (45 mm ahead of the profile centre, assumed) | right (-y) face, front-most slot, mirror of I1 |
| CAD reference | `arm_profile_link` (openamr-upperbody-sw); proposed node `slot_cover_left` | `arm_profile_link`; proposed node `slot_cover_right` |
| Height | from about 5 mm above the adapter plate (849 mm above the floor at lift 0) to about 5 mm below the J1_A plate | same |
| Approximate size | 8 mm slot; visible width about 8 to 10 mm; length about 85 mm in the preview, set from the J1_A plate outline (verify) | same |
| Material | extruded PVC or PP slot cover for a 6 series 8 mm slot; printed TPU strip if the colour is not offered | same |
| Colour | RAL 5018 (cyan reference, verify against a physical sample), coloured in the material | same |
| Attachment | pushed into the slot by hand; no adhesive, no new holes | same |
| Removal | pulled out by hand or with a plastic lever; the slot is reusable at once | same |
| Fit checks | strip holds in the anodised slot without tools; does not stand proud of the face by more than 1 mm; clears the J1_A plate and its 1 mm spacer; does not cross a cable route; not within 150 mm of the chest E-stop (K1) | same |
| Status | verify | verify |

### I3, OpenArm printed inserts (orange)

| Field | Value |
|---|---|
| Location | to be identified: only OpenArm 2.0 parts that the Enactic 2.0 BOM or CAD lists as printed, cosmetic and non-structural |
| CAD reference | `openarm_{left,right}_*` links of `enactic/openarm_description` `81fe647`; part names from the Enactic 2.0 BOM |
| Approximate size | per identified part |
| Material | the same material as the delivered part (the public 2.0 documentation does not list printed parts; the 1.0 leader end effector, an offboard capture device, is printed in PLA) |
| Colour | RAL 2004 orange filament, one accent colour only |
| Attachment | replaces the delivered part one for one, same fasteners; nothing added |
| Removal | the delivered part is kept as the spare and can be refitted |
| Licence | Enactic hardware files are CERN-OHL-S-2.0 (enactic/openarm_hardware); keep their notices with any reprint file |
| Fit checks | fit, function and strength equal to the delivered part; no change to the gripper or camera field of view; not within 150 mm of the chest E-stop (K1) |
| Status | verify: printed parts not identified; if none are printed, I3 is dropped and the robot carries the two cyan strips only |

## Keep-out rule K1 (safety colours)

| Device | Where | Colour kept | Keep-out |
|---|---|---|---|
| S2 chest E-stop (OpenArm kit button, two NC contacts) | mast, verify | red on yellow as delivered | no orange or cyan within 150 mm of the bezel edge; no accent on the face that carries it |
| S1 base E-stop | mobile base front panel | red on yellow | as above (no accents on the base) |
| RESET button XB4BW36B5 | mobile base, verify | standard blue | as above |

The 150 mm distance is a proposal of this plan, not a standard value; the safety owner may set another.

## Trims considered and not used

| Trim | Reason |
|---|---|
| Third slot strip on the front face | the front face has two slots; one must stay free and the chest E-stop or cable route may use the other |
| Strips on the rear face | both rear slots carry the rear upright T-nuts |
| Inserts, film or paint on the lift column | purchased telescoping column; never touched |
| Profile end caps | both profile ends are used (adapter plate below, camera bracket above) |
| Rubber edge protectors, bumper strips | excluded by the brief |
| Coloured parts on the head camera or its supplied mount | lenses and supplied parts stay as delivered |
