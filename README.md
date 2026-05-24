# Kartik Dangi

Robotics engineer focused on aerial perception — specifically extracting usable 3D maps from 4D FMCW radar on a UAV, in GPS-denied indoor environments, on embedded compute. No clean lab, no ground truth, no cheating.

**M.Eng. Elektro- und Informationstechnik** @ [THWS Schweinfurt](https://www.thws.de/)  
**B.Eng. Robotics** @ THWS — thesis: radar-based indoor mapping with a Continental ARS548 on an Avular Vertex One UAV  
**Working Student** @ [TTZ-EMO](https://www.thws.de/forschung/institute/ttz-emo/) — multithreaded PyQt5 toolchains for FEM simulation pipelines

---

## What I'm building

**[radar-indoor-mapping-uav](https://github.com/Kartikdangi1/radar-indoor-mapping-uav)**  
Containerized ROS 2 SLAM stack fusing 4D radar + camera for UAV navigation on NVIDIA Jetson. Radar gives you sparse, noisy point clouds in GPS-denied space — making something reliable out of that is harder than it looks.

**[ros2-autonomous-explorer](https://github.com/Kartikdangi1/ros2-autonomous-explorer)**  
Frontier-based exploration framework with a PPO policy for navigation decisions. Mostly a testbed for RL-on-hardware ideas — getting Stable Baselines 3 to behave sensibly on physical robots requires more tuning than the papers suggest.

---

## Stack

Most of what I do is **ROS 2 · C++ · Python** on Linux, containerized with Docker, deployed on Jetson hardware.

Perception & planning: `ROS 2/1` `Gazebo` `MoveIt` `PCL` `OpenCV` `SLAM` `Sensor Fusion`  
ML: `PyTorch` `Stable Baselines 3` `scikit-learn`  
Tooling: `Docker` `CMake` `Git` `NVIDIA Jetson` `PyQt5`  
Simulation & FEM: `Gmsh` `GetDP` `ONELAB` `Simscape`

---

## A few things worth mentioning

- Built `fused_odometry` and `temporal_radar_mapping` from scratch for the thesis platform — fusing Madgwick AHRS, lidar height EMA filtering, and ARS548 Doppler ego-velocity via RANSAC after discovering GNSS, magnetometer, and internal CreOS odometry were all non-functional on the drone
- Ported RMP2 motion planning to ROS 2 for a Neura Robotics MAiRA 7-DoF arm — real-time collision-free grasping at 30 FPS, fixed eye-to-hand camera at ~100 Hz
- Cut FEM simulation runtime by 50% through multithreaded processing and algorithm work at TTZ-EMO
- Designed and built the full UAV sensor payload: 3D-printed mounts, shielded harnesses, VLAN-segmented networking

---

## Get in touch

[LinkedIn](https://www.linkedin.com/in/kartik-dangi/) · [kartikdangide@gmail.com](mailto:kartikdangide@gmail.com)

---

<details>
<summary>GitHub Stats</summary>
<br>

![Kartik's GitHub Stats](https://github-readme-stats.vercel.app/api?username=Kartikdangi1&show_icons=true&theme=tokyonight&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Kartikdangi1&layout=compact&theme=tokyonight&hide_border=true)

</details>
