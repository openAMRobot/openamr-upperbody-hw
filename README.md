# openamr-upperbody-hw

Upper-body hardware for OpenAMRobot 2.0: the custom fixed mast, arm mounts, equipment brackets and cable routing on the mobile platform. An actuated lift is deferred to OpenAMRobot 3.0.

> **Status:** Design and integration scope. This repository does not yet provide a released mast design or fabrication/commissioning evidence.

## Current deliverables
- **Custom fixed mast:** COTS aluminium profiles, laser-cut or bent aluminium sheet and ready-made brackets. No welding or machining at the build site. The OpenArm 2.0 supplier body is not used.
- **Chassis interface:** base plate bolted into the chassis structural frame, with documented load path, fasteners and tightening torques.
- **Arm mounting:** shoulder bracket preserving the official OpenArm arm-mount frames, with 50 mm indexed adjustment and an index table.
- **Equipment mounting:** head camera, chest E-stop and operator equipment brackets, service access and cable strain relief.
- **Cable routing:** separated power/signal routes, service loops and labelled keyed deck disconnects.
- **Release package:** CAD, drawings, BOM, assembly instructions, mass/CoG, stiffness and stability evidence, assembled-height and sensor-clearance checks.
- **Lift module:** separate OpenAMRobot 3.0 scope.

## Mast and equipment allocation
The preliminary shoulder-axis height is **1400 mm above the floor** (`mast_1400`). **Maximum assembled height is 1700 mm**, including the head camera and all mounted equipment. Final shoulder position and permissible index positions require A4 and F2S evidence.

Central electronics, controllers, hubs and converters stay inside the mobile platform. The mast carries the arms, head camera, chest E-stop, operator equipment and cable routing; electronics integral to those devices remain part of the devices. No separate mast electronics/junction plate is part of this baseline.

## Interfaces
- Chassis structure, protected power branches and deck connectors are coordinated with `openamr-platform-hw`.
- Arm communication follows Jetson USB-CAN-FD adapters to the OpenArm kit. CAN 1 is reserved for STM32-to-drive communication; isolated CAN 2 serves STM32-to-BMS communication. Do not add upper-body devices to either base bus. No RS485.
- Provide mounting transforms, geometry and mass properties to `openamr-upperbody-sw` for the combined model and configuration metadata.

## This cycle
Custom fixed-mast design, mounting and physical integration are current OpenAMRobot 2.0 work. Fabrication and commissioning follow the approved work-package gates; their completion requires evidence and is not implied by this README. The lift remains deferred to OpenAMRobot 3.0.

Part of the OpenAMRobot ecosystem: https://github.com/openAMRobot

## Ownership, licensing, and contributions

OpenAMRobot is a project initiated, operated, and controlled by **Botshare LTD** (Cyprus Company ID HE479056). Botshare LTD owns the transferable economic rights in original OpenAMRobot material created by or validly assigned to it. Third-party material remains subject to its respective ownership, licences, and notices.

Original OpenAMRobot software and firmware are licensed under MIT, documentation under CC BY 4.0, and hardware design source under CERN-OHL-P-2.0, as mapped in [`LICENSING.md`](LICENSING.md). Public distribution grants the permissions stated in the applicable licence; it does not transfer ownership of underlying copyright, trademarks, patents, or other intellectual property.

Accepted external contributions require DCO sign-off and an applicable Individual or Corporate Contributor Agreement. See the organization [IP Policy](https://github.com/openAMRobot/.github/blob/main/IP_POLICY.md), [Contribution Guide](https://github.com/openAMRobot/.github/blob/main/CONTRIBUTING.md), and [Contributor Agreement Process](https://github.com/openAMRobot/.github/blob/main/CLA.md).
