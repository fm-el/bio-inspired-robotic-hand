# bio-inspired-robotic-hand
Design of a bio-inspired, tendon-driven robotic hand. Academic project exploring underactuation and tendon routing, inspired by research on existing architectures. Work in progress.

**Status:**  Work in progress — mechanical design phase

## Project Overview

This project aims to design and build an anthropomorphic robotic hand capable of reproducing 
essential human hand movements (flexion, extension, thumb opposition) for autonomous grasping 
tasks in unstructured environments (where object position, shape, and nature are not known in advance).
This work is carried out as part of my engineering curriculum in the Autonomous Systems field, over the 2026-2027 academic year.

## Objectives

- Achieve stable grasping of objects with varied shapes (power grip & precision grip)
- Detect contact and applied force on manipulated objects
- Adapt grip force according to the nature of the grasped object
- Coordinate finger motion through mechanical/motion synergies
- Integrate visual perception for object recognition (long-term goal)

## Approach

The design is based on an extensive bibliographic study of existing robotic hands 
(DLR-HIT Hand II, Pisa/IIT SoftHand, Seed Robotics RH8D, ORCA Hand, Bionic Hand Delta 1.1), 
leading to the following architecture choices:

- **17 degrees of freedom driven by 9 actuators**, using mechanical coupling (synergies) on long fingers
- **Tendon-driven transmission** (nylon tendons + PTFE sheaths), inspired by human finger biomechanics
- **Independent thumb actuation** (MCP + IP) for fine opposition grasps
- **Force + position sensor fusion** (FSR + SV01A) for closed-loop grasp control
- **PETG** as primary structural material (3D printed parts)

Full bibliographic report: [`rapport-bibliographique-2026-2027.pdf`](rapport-bibliographique-2026-2027.pdf)

## Hardware (planned)

| Category | Components |
|---|---|
| Actuation | 6× MG996 servo (15 kg.cm) — flexion, 3× MG90S — abduction |
| Sensing | 5× FSR 0.2" (force), 14× SV01A (position) |
| Electronics | ESP32 DevKit V2, NVIDIA Jetson Nano, PCA9685, Logitech C505e camera |
| Mechanical | Nylon tendons, 2mm PTFE sheaths, PETG 3D-printed structure |
| Power | 6V / 10-15A external supply |

## Roadmap

- [x] Literature review & architecture selection
- [x] Requirements definition (SysML diagrams)
- [ ] Mechanical design (Fusion 360) — *in progress*
- [ ] 3D printing & first prototype assembly
- [ ] Sensor integration & wiring
- [ ] Low-level control (force + position feedback loop)
- [ ] Motion synergies implementation
- [ ] Visual perception integration
- [ ] Learning-based grasp strategy selection (long-term)

## References

Key research references used in the design process are listed in the bibliographic report.
