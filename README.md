# openamr-upperbody-hw

Upper-body hardware for the OpenAMRobot mobile manipulator: mechanics and electrical design for the lift and arm mounts on the mobile base.

> **Status:** Planned, no code yet

Populated next cycle, after simulation validates the geometry. This repository currently holds only this README.

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
