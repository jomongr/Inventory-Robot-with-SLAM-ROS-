# 📦 Inventory-Bot: Autonomous Warehouse Navigator

![ROS](https://img.shields.io/badge/ROS-Noetic/Melodic-blue?style=for-the-badge&logo=ros)
![Python](https://img.shields.io/badge/Python-3.7+-yellow?style=for-the-badge&logo=python)
![Gazebo](https://img.shields.io/badge/Simulation-Gazebo-orange?style=for-the-badge)

Inventory-Bot is an autonomous mobile robotics platform designed for smart warehousing. Leveraging **SLAM**, **Sensor Fusion**, and a **custom URDF**, this bot navigates complex environments and utilizes a Python-controlled adjustable tray to deliver items to specific vertical heights.

---

## 🚀 Key Features
- **Autonomous Navigation:** Full integration with the ROS Navigation Stack for global and local path planning.
- **Dynamic SLAM:** Real-time mapping and localization using LiDAR and RGB camera data.
- **Vertical Actuation:** A custom-designed prismatic tray system for tiered shelf delivery.
- **Precision Perception:** Extended Kalman Filter (EKF) for fused, low-noise odometry.
- **Simulation-Ready:** Pre-configured Gazebo environments and RViz visualizations for testing.

---

## 🛠️ System Architecture

### 🛰️ Perception & Navigation
- **LiDAR:** 360° environment scanning for obstacle avoidance.
- **EKF Node:** Fuses IMU, wheel odometry, and LiDAR data for stable localization.
- **SLAM:** Uses GMapping/Cartographer to generate high-resolution occupancy grids.

### 🏗️ Hardware Design (URDF)
- **Base:** Differential drive mobile platform.
- **Tray Actuator:** Python-driven prismatic joint for Z-axis movement.
- **Sensors:** Integrated LiDAR and RGB Camera with realistic noise models.

---

## 🎮 Usage

### 1. Set Initial Pose
Align the robot's localization with its Gazebo coordinates:
```bash
python set_initial_pose.py
