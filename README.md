# Kartik Dangi

Robotics engineer working on aerial perception and robot learning: useful 3D maps from 4D FMCW radar on a UAV in GPS-denied indoor spaces, and human-in-the-loop reinforcement learning that holds up on real hardware. Sensor fusion, ROS 2, and embedded compute. No clean lab, no ground truth.

**M.Sc. Mechatronics, Robotics & Biomechanical Engineering** · [TUM](https://www.tum.de/), from Oct 2026  
**M.Eng. Elektro- und Informationstechnik** · [THWS Schweinfurt](https://www.thws.de/), research: UAV radar-camera fusion on a Jetson Orin NX  
**B.Eng. Robotics** · THWS, thesis (1.3): radar-based indoor mapping with a Continental ARS548 on an Avular Vertex One  
**Robotics Software Intern** · Fraunhofer IIS, Adaptive Robotics Research, Dresden: the PySide6/ROS 2 operator interface for a HIL-SERL robot-learning pipeline  
**Portfolio** · [kartikdangi1.github.io/Portfolio](https://kartikdangi1.github.io/Portfolio/), project pages with demo videos, figures and pipeline breakdowns  
**Resume** · [English](https://kartikdangi1.github.io/Portfolio/assets/resume.pdf) · [Deutsch](https://kartikdangi1.github.io/Portfolio/assets/resume-de.pdf)  

Open to working-student roles alongside the TUM M.Sc.

---

## Selected work

Much of this is university or institutional work, or in private repositories, so the project pages on the [portfolio](https://kartikdangi1.github.io/Portfolio/#projects) are the place to see it: demo videos, figures and how each pipeline works.

**[Radar-Based Indoor Mapping for UAVs](https://kartikdangi1.github.io/Portfolio/projects/radar-indoor-mapping-uav/)**  
Bachelor's thesis: a ROS 2 system that turns a Continental ARS548 4D radar into real-time indoor occupancy mapping for a UAV. No GPS, no camera, no LiDAR map. Radar Doppler, IMU and downward LiDAR are fused into dead-reckoning odometry at 50 Hz (1.9 % endpoint drift over 71 m in a room, 3.7 % over 331 m in a corridor) that feeds GICP SLAM with loop closure. A separate radar path builds a temporal Bayesian occupancy grid with a three-stage multipath filter removing over 95 % of spurious reflections. Under 22 % mean CPU and 100 MB RAM on the UAV's Jetson Orin NX.

**[HIL-SERL Lite](https://kartikdangi1.github.io/Portfolio/projects/hil-serl-lite/)**  
From-scratch reimplementation of HIL-SERL (human-in-the-loop, sample-efficient robot RL): hand-written SAC in JAX/Flax, RLPD dual-buffer replay, HG-DAgger intervention routing, in MuJoCo. It grew into a research platform with YAML-declared tasks, a one-command demos-to-train-to-eval pipeline, and 20+ switchable RL methods, and it is the subject of my semester report: six robot arms behind one registry, a 7.74x faster flow-matching policy via consistency distillation, a training collapse (70 % to 0 % success) diagnosed and fixed with per-stage skill chaining, and 86.7 % success on a LIBERO benchmark task trained from scratch.

**[Sinew](https://kartikdangi1.github.io/Portfolio/projects/sinew/)**  
The shared ROS 2 library behind seven robotics packages: MoveIt motion planning, pybind11 bridges to MoveIt 2's time-optimal trajectory generation and Ruckig smoothing, a MoveIt Servo lifecycle manager, admittance force control, and one client interface across Franka, OnRobot and Schunk grippers.

**[Radar-Camera Fusion & Tracking for UAVs](https://kartikdangi1.github.io/Portfolio/projects/drone-radar-camera-fusion/)** *(ongoing, Master's research)*  
A Continental ARS548 4D radar and an Intel RealSense D435i on an Avular Vertex One (Jetson Orin NX), brought up over gPTP-synchronised automotive Ethernet. Dockerised Kalibr and corner-reflector radar-camera calibration, then Hungarian-matching fusion and a ByteTrack-based tracker that uses radar Doppler velocity directly in its Kalman update.

**[Interactive Distance Field Mapping & Planning (IDMP)](https://kartikdangi1.github.io/Portfolio/projects/idmp-cobot/)**  
Migrated a ROS 1 collision-avoidance stack (6-DoF UR5e) to ROS 2 for a 7-DoF NEURA MAiRA cobot at CERI (THWS): Azure Kinect with a TF2 self-filter and 18 virtual collision points, and null-space motion that reacts to moving obstacles at a stable 98-100 Hz instead of pausing to re-plan. Added a MediaPipe hand-gesture interface for hands-free assembly steps.

**[Vision-Guided Robotic Socket Insertion](https://kartikdangi1.github.io/Portfolio/projects/vision-guided-socket-insertion/)**  
Assembly cell guided entirely by vision: Detectron2 segmentation, SIFT + RANSAC pose refinement, and a live reward classifier confirming each insertion. 0.964 mean mask IoU on 34 validation instances; 25 of 27 insertion cycles with no manual correction in a 30-minute session.

Also on the portfolio: an [autonomous frontier explorer](https://kartikdangi1.github.io/Portfolio/projects/ros2-autonomous-explorer/).

---

## Stack

Most of what I do is **ROS 2 · C++ · Python** on Linux, containerised with Docker, deployed on Jetson hardware.

**Robotics & Perception** · `ROS 2/1` `Gazebo` `MoveIt` `Nav2` `PCL` `OpenCV` `SLAM` `Sensor Fusion` `4D Radar` `PX4/MAVLink`  
**ML & RL** · `PyTorch` `JAX/Flax` `MuJoCo` `Stable Baselines 3` `Detectron2` `MediaPipe`  
**Tooling** · `Docker` `CMake` `Git` `GitHub Actions` `GitLab CI` `NVIDIA Jetson` `PySide6/Qt` `Linux`  
**Simulation & FEM** · `Gmsh` `GetDP` `ONELAB` `Simscape`

---

## A few things worth mentioning

- Built the PySide6 + ROS 2 operator interface for a HIL-SERL pipeline at Fraunhofer IIS: rebuilt its backend into a layered architecture over 40 ROS 2 services, eliminated 8 Qt threading crash classes, and wrote an MCP server that exposes robot path planning as LLM-callable endpoints
- Built `fused_odometry` and `temporal_radar_mapping` from scratch after GNSS, magnetometer and the platform's own odometry all turned out to be non-functional
- Ported RMP2 motion planning to ROS 2 for a 7-DoF NEURA MAiRA arm: real-time collision-free grasping at 30 FPS with a fixed eye-to-hand camera at about 100 Hz
- Ported the GetDP electromagnetic solver to Windows and sped up FEM simulation by about 40 % with multithreading at TTZ-EMO
- Designed the UAV sensor payload end to end: 3D-printed mounts, a dual-power interface board, shielded harnesses, VLAN-segmented networking

---

## Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Kartikdangi1/Kartikdangi1/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Kartikdangi1/Kartikdangi1/output/github-contribution-grid-snake.svg" />
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Kartikdangi1/Kartikdangi1/output/github-contribution-grid-snake.svg" />
</picture>

[![GitHub Stats](https://github-readme-stats-rickstaa.vercel.app/api?username=Kartikdangi1&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)](https://github.com/anuraghazra/github-readme-stats)
[![Top Langs](https://github-readme-stats-rickstaa.vercel.app/api/top-langs/?username=Kartikdangi1&layout=compact&theme=tokyonight&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)

[![GitHub Streak](https://streak-stats.demolab.com?user=Kartikdangi1&theme=tokyonight&hide_border=true&card_width=500)](https://git.io/streak-stats)

---

## Get in touch

[![Portfolio](https://img.shields.io/badge/Portfolio-kartikdangi1.github.io-124D54?style=flat&logo=githubpages&logoColor=white)](https://kartikdangi1.github.io/Portfolio/)
[![Resume](https://img.shields.io/badge/Resume-PDF-094044?style=flat&logo=readthedocs&logoColor=white)](https://kartikdangi1.github.io/Portfolio/assets/resume.pdf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kartik--dangi-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kartik-dangi/)
[![Email](https://img.shields.io/badge/Email-kartikdangide@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:kartikdangide@gmail.com)
