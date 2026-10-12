# openamr-upperbody-hw

Upper-body hardware for OpenAMRobot 2.0: the lift column on a two-position base plate, the arm profile and arm mounts, equipment brackets and cable routing on the mobile platform.

> **Status:** Design and integration scope. This repository does not yet provide a released upper-body design or fabrication/commissioning evidence.

## Current deliverables
- **Lift column:** DOLD Hexalift V4, 350 mm stroke (530 mm retracted, 880 mm extended), mounted with its 240 mm side fore-aft. The OpenArm 2.0 supplier body is not used.
- **Base plate:** 10 mm aluminium on the 294 mm chassis deck (top face 304 mm), with two fore-aft column positions, `bp000` (column axis 330 mm behind the chassis front edge, x +0.060) and `bp050` (+50 mm).
- **Chassis interface:** base plate bolted to the chassis deck, with documented load path, fasteners and tightening torques.
- **Arm mounting:** a MISUMI HFS6-60120 arm profile, 340 mm long, standing on a 10 mm adapter plate on the column top. The OpenArm 2.0 J1_A plates bolt to its side T-slots, preserving the official arm-mount frames; the arm mount point is 180 mm ahead of the column axis.
- **Equipment mounting:** head camera (ZED Mini on the lift carriage), chest E-stop and operator equipment brackets, service access and cable strain relief.
- **Cable routing:** separated power/signal routes, service loops, lift-travel cable management and labelled keyed deck disconnects.
- **Release package:** CAD, drawings, BOM, assembly instructions, mass/CoG, stiffness and stability evidence, assembled-height and sensor-clearance checks.

## Upper-body layout
The decided values, the height stack, the fastening and the head-camera bracket are recorded in [`docs/mechanical/upper_body_option_B.md`](docs/mechanical/upper_body_option_B.md). Decision of record: P-03 revision 19.0 items 16 to 19, 12 October 2026 (option B).

Heights are from the floor (Z = 0). The shoulder, at the OpenArm arm mount point, is 304 + 530 + 166 = **1000 mm** with the lift retracted and 304 + 880 + 166 = **1350 mm** fully extended. The lift height is joint state; `L1000`, `L1175` and `L1350` are calibration stops. **1700 mm is the maximum complete assembled robot height** at full lift extension, including the head camera and all mounted equipment.

Configuration IDs: `column` (`dold_v4_350`, `tl3_400`), `base_plate` (`bp000`, `bp050`), `head_pitch` (`hp15` to `hp35`, baseline `hp25`), `base_tilt` (`bt05`, `bt10`, `bt15`).

Central electronics, controllers, hubs and converters stay inside the mobile platform. The lift carriage carries the arms, head camera and chest E-stop; electronics integral to those devices remain part of the devices.

## Interfaces
- Chassis structure, protected power branches and deck connectors are coordinated with `openamr-platform-hw`.
- Arm communication follows Jetson USB-CAN-FD adapters to the OpenArm kit. CAN 1 is reserved for STM32-to-drive communication; isolated CAN 2 serves STM32-to-BMS communication. Do not add upper-body devices to either base bus. No RS485.
- Provide mounting transforms, geometry and mass properties to `openamr-upperbody-sw` for the combined model and configuration metadata.

## This cycle
Lift-column mounting, base plate, arm profile, brackets and physical integration are current OpenAMRobot 2.0 work. Supplier hole patterns and outlines are pending supplier CAD. Lift holding on E-stop and power loss, the lift driver and interface, and the stability rerun for both base-plate positions are open release gates owned elsewhere. Fabrication and commissioning follow the approved work-package gates; their completion requires evidence and is not implied by this README.

Part of the OpenAMRobot ecosystem: https://github.com/openAMRobot

## Ownership, licensing, and contributions

OpenAMRobot is a project initiated, operated, and controlled by **Botshare LTD** (Cyprus Company ID HE479056). Botshare LTD owns the transferable economic rights in original OpenAMRobot material created by or validly assigned to it. Third-party material remains subject to its respective ownership, licences, and notices.

Original OpenAMRobot software and firmware are licensed under MIT, documentation under CC BY 4.0, and hardware design source under CERN-OHL-P-2.0, as mapped in [`LICENSING.md`](LICENSING.md). Public distribution grants the permissions stated in the applicable licence; it does not transfer ownership of underlying copyright, trademarks, patents, or other intellectual property.

Accepted external contributions require DCO sign-off and an applicable Individual or Corporate Contributor Agreement. See the organization [IP Policy](https://github.com/openAMRobot/.github/blob/main/IP_POLICY.md), [Contribution Guide](https://github.com/openAMRobot/.github/blob/main/CONTRIBUTING.md), and [Contributor Agreement Process](https://github.com/openAMRobot/.github/blob/main/CLA.md).
