# Kartik Dangi

Robotics engineer focused on aerial perception — getting useful 3D maps out of 4D FMCW radar on a UAV, in GPS-denied indoor environments, on embedded compute. No clean lab, no ground truth.

**M.Eng. Elektro- und Informationstechnik** · [THWS Schweinfurt](https://www.thws.de/)  
**B.Eng. Robotics** · THWS — thesis: radar-based indoor mapping with a Continental ARS548 on an Avular Vertex One  
**Working Student** · [TTZ-EMO](https://www.thws.de/forschung/institute/ttz-emo/) — multithreaded PyQt5 toolchains for FEM simulation pipelines  
**Portfolio** · [kartikdangi1.github.io/Portfolio](https://kartikdangi1.github.io/Portfolio/) — write-ups, demo videos and pipeline breakdowns for everything below

---

## Selected work

A mix of public repos and university/institutional work. Full write-ups, demo videos and pipeline diagrams for all of it — including autonomous exploration, phone-as-sensor drone control, and hand tracking — are on the [portfolio](https://kartikdangi1.github.io/Portfolio/#projects).

**[Radar-Based Indoor Mapping for UAVs](https://github.com/Kartikdangi1/radar-indoor-mapping-uav)**  
Bachelor's thesis: a ROS 2 system that turns a Continental ARS548 4D radar into real-time indoor occupancy mapping for a UAV — no GPS, no camera, no LiDAR map. Fused odometry (Madgwick IMU + RANSAC Doppler ego-velocity + LiDAR height) feeds a GICP SLAM pipeline with loop closure, while a separate radar path builds a temporal Bayesian occupancy grid with occlusion filtering. End to end in ~150 ms on a Jetson Orin NX.

**Interactive Distance Field Mapping & Planning (IDMP)** — *[demo & write-up on the portfolio](https://kartikdangi1.github.io/Portfolio/#projects)*  
Migrated a ROS 1 collision-avoidance stack (6-DoF UR5e) to ROS 2 for a 7-DoF NEURA MAiRA cobot at CERI (THWS). Rebuilt the pipeline around an Azure Kinect with a TF2 self-filter and 18 virtual collision points, using null-space exploitation to react to moving obstacles at a stable 98–100 Hz instead of pausing to re-plan. Added a MediaPipe hand-gesture interface so an operator can step through an assembly sequence hands-free.

**[HIL-SERL Lite](https://github.com/Kartikdangi1/hil_serl_lite)**  
From-scratch reimplementation of HIL-SERL (human-in-the-loop, sample-efficient robot RL): hand-written SAC in JAX/Flax, RLPD dual-buffer replay, HG-DAgger intervention routing, against a simulated Franka Panda in MuJoCo. Grew into a small research platform — YAML-declared tasks, a one-command demos→train→eval pipeline with a web dashboard, and 20+ swappable RL methods benchmarked head-to-head, backed by 112+ tests.

**[Radar-Camera Fusion & Tracking for UAVs](https://github.com/Kartikdangi1/drone-radar-camera-fusion)** *(ongoing — Master's thesis)*  
Fusing a Continental ARS548 4D radar with an Intel RealSense D435i for multi-object tracking in flight: a Hungarian-matching fusion node, a ByteTrack-based tracker that uses radar Doppler velocity directly in its Kalman update, and gPTP hardware time-sync between sensors — running on an Avular Vertex One (Jetson Orin NX).

**Vision-Guided Robotic Socket Insertion** — *[demo & write-up on the portfolio](https://kartikdangi1.github.io/Portfolio/#projects)*  
Assembly cell that performs socket insertion guided entirely by vision: a Detectron2 segmentation model locates the part, SIFT + RANSAC refines its pose, and a live vision-based reward classifier confirms each insertion. 0.964 mean mask IoU across 34 validation instances; 25 of 27 insertion cycles completed with no manual correction in a 30-minute session.

---

## Stack

Most of what I do is **ROS 2 · C++ · Python** on Linux, containerized with Docker, deployed on Jetson hardware.

**Robotics & Perception** · `ROS 2/1` `Gazebo` `MoveIt` `PCL` `OpenCV` `SLAM` `Sensor Fusion` `4D Radar` `PX4/MAVLink`  
**ML & RL** · `PyTorch` `JAX/Flax` `Stable Baselines 3` `scikit-learn` `Detectron2` `MediaPipe`  
**Tooling** · `Docker` `CMake` `Git` `NVIDIA Jetson` `PyQt5` `Linux`  
**Simulation & FEM** · `Gmsh` `GetDP` `ONELAB` `Simscape`

---

## A few things worth mentioning

- Built `fused_odometry` and `temporal_radar_mapping` from scratch — fusing Madgwick AHRS, lidar height EMA filtering, and ARS548 Doppler ego-velocity via RANSAC, after GNSS, magnetometer, and internal CreOS odometry all turned out to be non-functional on the platform
- Ported RMP2 motion planning to ROS 2 for a Neura Robotics MAiRA 7-DoF arm — real-time collision-free grasping at 30 FPS, fixed eye-to-hand camera running at ~100 Hz
- Cut FEM simulation runtime by 50% through multithreaded processing and algorithm work at TTZ-EMO
- Designed the full UAV sensor payload: 3D-printed mounts, shielded harnesses, VLAN-segmented networking

---

## Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Kartikdangi1/Kartikdangi1/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Kartikdangi1/Kartikdangi1/output/github-contribution-grid-snake.svg" />
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Kartikdangi1/Kartikdangi1/output/github-contribution-grid-snake.svg" />
</picture>

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Kartikdangi1&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)](https://github.com/anuraghazra/github-readme-stats)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Kartikdangi1&layout=compact&theme=tokyonight&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)

[![GitHub Streak](https://streak-stats.demolab.com?user=Kartikdangi1&theme=tokyonight&hide_border=true&card_width=500)](https://git.io/streak-stats)

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Kartikdangi1&bg_color=1a1b27&color=70a5fd&line=bf91f3&point=38bdae&area=true&hide_border=true)](https://github.com/ashutosh00710/github-readme-activity-graph)

---

## Get in touch

[![Portfolio](https://img.shields.io/badge/Portfolio-kartikdangi1.github.io-FF5D3D?style=flat&logo=githubpages&logoColor=white)](https://kartikdangi1.github.io/Portfolio/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kartik--dangi-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kartik-dangi/)
[![Email](https://img.shields.io/badge/Email-kartikdangide@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:kartikdangide@gmail.com)
