<div align="center">

# :ocean: OAT-UUV

### Design of an Underwater Vehicle with Orientation-Adjustable Thrusters

**Yifei Wang<sup>*</sup>, Shihan Kong<sup>*</sup>, Zhanhua Xin, Kaiwei Zhu, and Junzhi Yu**

<sup>*</sup> Equal contribution

[[`Paper`](https://arxiv.org/pdf/2503.19288)] [[`BibTeX`](#black_nib-citation)]

</div>

## :memo: Introduction

OAT-UUV is a compact underwater vehicle equipped with four **orientation-adjustable thrusters (OATs)**. Each thruster can rotate independently, allowing the vehicle to continuously redirect its thrust vectors and generate forces and moments in all six degrees of freedom. This configuration enables surge, sway, heave, roll, pitch, yaw, and coupled maneuvers with only four thrusters.

The vehicle uses a streamlined Myring-curve hull to reduce hydrodynamic drag while maintaining a compact and portable platform. For target tracking, the system combines an onboard vision module with a **feedforward adaptive model predictive controller (FF-AMPC)**. The controller updates its model parameters online, predicts future target motion, and compensates for uncertain hydrodynamics and external disturbances.

This repository provides the mechanical and electrical design resources for OAT-UUV. The upper- and lower-computer software is maintained in the separate repositories linked below.

## :bulb: Highlights

- **Four orientation-adjustable thrusters.** Four independently rotating vector thrusters dynamically reshape the vehicle's propulsion directions.
- **Full six-DOF maneuverability.** The platform supports independent and coupled translational and rotational motions with only four thrusters.
- **Compact streamlined design.** The Myring-curve hull measures approximately **60.7 cm x 50.2 cm x 20.3 cm** and the complete vehicle weighs approximately **9.2 kg**.
- **Vision-based target tracking.** An onboard camera detects and tracks underwater targets in real time.
- **Feedforward adaptive MPC.** FF-AMPC combines trajectory prediction, online model adaptation, and model predictive control for robust tracking under uncertain underwater dynamics.
- **Robust hovering.** Disturbance experiments reported in the paper show a **49.1% improvement in hovering stability** compared with a conventional controller.
- **Real-world validation.** Experiments include basic motion, in-place rotation, coupled maneuvers, disturbance rejection, and visual tracking of a robotic manta ray.
- **Open hardware resources.** This repository includes the complete STEP assembly and the power-distribution PCB design files.

## :fire: News

- **`2026/11/15`**: We release the OAT-UUV hardware resources, including the complete 3D model and power-distribution PCB design.
- **`2026/11/03`**: The revised paper is released on arXiv.
- **`2026/03/05`**: The paper is accepted by *IEEE/ASME Transactions on Mechatronics*.
- **`2025/03/25`**: The first version of the OAT-UUV paper is released on arXiv.

## :package: Project Contents

### Hardware Resources

| Category | Resource | Description |
| --- | --- | --- |
| Mechanical design | [`Structure/Total structure.STEP`](Structure/Total%20structure.STEP) | Complete 3D assembly of the OAT-UUV in STEP format. |
| Electrical design | [`Electrical/Power distribution.zip`](Electrical/Power%20distribution.zip) | Power-distribution board source files, including the Altium schematic (`P1.schdoc`) and PCB layout (`PCB1.pcbdoc`). |

### Software Repositories

| Component | Repository | Description |
| --- | --- | --- |
| Lower computer | [auv-v4.1-board](https://gitee.com/walker_632/auv-v4.1-board) | Board-side firmware and device drivers. |
| Upper computer | [auv-v4-nx](https://gitee.com/walker_632/auv-v4-nx) | NVIDIA Jetson NX host software, vision modules, and drivers. |

### Repository Structure

```text
oat-uuv/
|-- Electrical/
|   `-- Power distribution.zip
|-- Structure/
|   `-- Total structure.STEP
|-- LICENSE
`-- README.md
```

## :movie_camera: Video Demos

The following demo slots correspond to the representative real-world experiments reported in the paper. Short videos will be added to this section.

| Demo | Content | Status |
| --- | --- | --- |
| Basic motion | Surge, sway, heave, and in-place rotation. | Coming soon |
| Combined motion I | Simultaneous heave, surge, and roll maneuver. | Coming soon |
| Combined motion II | Simultaneous surge and pitch maneuver. | Coming soon |
| Disturbance rejection | Hovering and recovery under external disturbances. | Coming soon |
| Underwater visual tracking | Closed-loop tracking of a robotic manta ray. | Coming soon |

<!--
Suggested layout after the videos are uploaded:

### Basic Motion
[Preview image or GIF](assets/videos/basic_motion.mp4)

### Combined Motion I: Heave-Surge-Roll
[Preview image or GIF](assets/videos/heave_surge_roll.mp4)

### Combined Motion II: Surge-Pitch
[Preview image or GIF](assets/videos/surge_pitch.mp4)

### Disturbance Rejection
[Preview image or GIF](assets/videos/disturbance_rejection.mp4)

### Underwater Visual Tracking
[Preview image or GIF](assets/videos/visual_tracking.mp4)
-->

## :black_nib: Citation

If you find this project useful for your research, please consider citing:

```bibtex
@article{wang2026design,
  title={Design of an Underwater Vehicle with Orientation-Adjustable Thrusters and Adaptive Tracking Control},
  author={Wang, Yifei and Kong, Shihan and Xin, Zhanhua and Zhu, Kaiwei and Yu, Junzhi},
  journal={IEEE/ASME Transactions on Mechatronics},
  year={2026},
  doi={10.1109/TMECH.2026.3672531}
}
```
