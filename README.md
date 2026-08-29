# openamr-upperbody-hw

Upper-body hardware for the OpenAMRobot mobile manipulator: mechanics and electrical design for the lift and arm mounts on the mobile base.

**Status:** planned. Populated next cycle, after simulation validates the geometry.

## What will live here
- **Lift module:** rails, actuator, carriage, mechanical drawings.
- **Mounting:** the arm mounting-plate interface, per-arm adapter plates, and the mount surface on the base.
- **End-effector mounts.**
- **Upper-body wiring and power distribution.**
- **Bill of materials and assembly documentation.**

## Interfaces
- Consumes a defined power and CAN or serial connector from `openamr-platform-hw`.
- Provides the mounting-plate frame that `openamr-upperbody-sw` models in the combined URDF.

## This cycle
Concept and make-or-buy analysis for the lift, plus the mounting-plate interface, informed by simulation. Physical build is next cycle.

Part of the OpenAMRobot ecosystem: https://github.com/openAMRobot

## Ownership, licensing, and contributions

OpenAMRobot is a project initiated, operated, and controlled by **Botshare LTD** (Cyprus Company ID HE479056). Botshare LTD owns the transferable economic rights in original OpenAMRobot material created by or validly assigned to it. Third-party material remains subject to its respective ownership, licences, and notices.

Public distribution under this repository's applicable licence grants the permissions stated in that licence; it does not transfer ownership of underlying copyright, trademarks, patents, or other intellectual property.

Accepted external contributions require DCO sign-off and an applicable Individual or Corporate Contributor Agreement. See the organization [IP Policy](https://github.com/openAMRobot/.github/blob/main/IP_POLICY.md), [Contribution Guide](https://github.com/openAMRobot/.github/blob/main/CONTRIBUTING.md), and [Contributor Agreement Process](https://github.com/openAMRobot/.github/blob/main/CLA.md).
