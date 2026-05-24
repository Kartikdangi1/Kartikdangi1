# Kartik Dangi

Robotics engineer focused on aerial perception — getting useful 3D maps out of 4D FMCW radar on a UAV, in GPS-denied indoor environments, on embedded compute. No clean lab, no ground truth.

**M.Eng. Elektro- und Informationstechnik** · [THWS Schweinfurt](https://www.thws.de/)  
**B.Eng. Robotics** · THWS — thesis: radar-based indoor mapping with a Continental ARS548 on an Avular Vertex One  
**Working Student** · [TTZ-EMO](https://www.thws.de/forschung/institute/ttz-emo/) — multithreaded PyQt5 toolchains for FEM simulation pipelines

---

## What I'm building

**[radar-indoor-mapping-uav](https://github.com/Kartikdangi1/radar-indoor-mapping-uav)**  
Containerized ROS 2 SLAM stack fusing 4D radar + camera for real-time UAV navigation on NVIDIA Jetson. The core problem: radar gives you sparse, noisy point clouds in GPS-denied space — making something reliable out of that is harder than it looks.

**[ros2-autonomous-explorer](https://github.com/Kartikdangi1/ros2-autonomous-explorer)**  
Frontier-based autonomous exploration with a PPO policy for navigation decisions. Mostly a testbed for RL-on-hardware ideas — getting Stable Baselines 3 to behave on physical robots takes more tuning than the papers suggest.

---

## Stack

Most of what I do is **ROS 2 · C++ · Python** on Linux, containerized with Docker, deployed on Jetson hardware.

**Robotics & Perception** · `ROS 2/1` `Gazebo` `MoveIt` `PCL` `OpenCV` `SLAM` `Sensor Fusion`  
**ML & RL** · `PyTorch` `Stable Baselines 3` `scikit-learn`  
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

[![GitHub Streak](https://streak-stats.demolab.com?user=Kartikdangi1&theme=tokyonight&hide_border=true&card_width=500)](https://git.io/streak-stats)

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Kartikdangi1&bg_color=1a1b27&color=70a5fd&line=bf91f3&point=38bdae&area=true&hide_border=true)](https://github.com/ashutosh00710/github-readme-activity-graph)

---

## Get in touch

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kartik--dangi-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kartik-dangi/)
[![Email](https://img.shields.io/badge/Email-kartikdangide@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:kartikdangide@gmail.com)
