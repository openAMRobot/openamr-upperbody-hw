# openamr-upperbody-hw

Upper-body hardware for OpenAMRobot 2.0: the custom fixed mast, arm mounts, equipment brackets and cable routing on the mobile platform. An actuated lift is deferred to OpenAMRobot 3.0.

> **Status:** Design and integration scope. This repository does not yet provide a released mast design or fabrication/commissioning evidence.

## Current deliverables
- **Custom fixed mast:** one COTS aluminium profile (MISUMI HFS6-60120) on a laser-cut base plate with ready-made brackets. No welding or machining at the build site. The OpenArm 2.0 supplier body is not used.
- **Chassis interface:** base plate bolted into the chassis structural frame, with documented load path, fasteners and tightening torques.
- **Arm mounting:** the OpenArm 2.0 J1_A plates bolt to the side T-slots of the mast profile, preserving the official arm-mount frames; four indexed positions with an index table.
- **Equipment mounting:** head camera, chest E-stop and operator equipment brackets, service access and cable strain relief.
- **Cable routing:** separated power/signal routes, service loops and labelled keyed deck disconnects.
- **Release package:** CAD, drawings, BOM, assembly instructions, mass/CoG, stiffness and stability evidence, assembled-height and sensor-clearance checks.
- **Lift module:** separate OpenAMRobot 3.0 scope.

## Mast and equipment allocation
The fixed-mast architecture, mast mounting and upper-body hardware integration are current OpenAMRobot 2.0 scope. The lift module, lift controller and lift requirements are deferred to OpenAMRobot 3.0.

The mast is one MISUMI HFS6-60120 aluminium profile with its top **1500 mm above the floor**, carrying four indexed shoulder-axis positions, 1300, 1350, 1400 and 1450 mm. The release configuration is `mast_1350`, a **1350 mm shoulder-axis height**. **1700 mm is the maximum complete assembled robot height**, including the head camera and all mounted equipment; the robot may be lower, never higher. It is not the shoulder-axis height. The other three positions are available for A4 reach tests and engineering analysis, not installed release configurations without a recorded decision. Decision of record: P-03 Decision Addendum revision 18.2, 28 September 2026.

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
