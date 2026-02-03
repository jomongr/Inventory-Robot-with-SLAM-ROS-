# 📦 Inventory-Bot: Autonomous Warehouse Navigator

![ROS](https://img.shields.io/badge/ROS-Noetic-blue?style=for-the-badge&logo=ros)
![Python](https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python)
![Gazebo](https://img.shields.io/badge/Simulation-Gazebo-orange?style=for-the-badge)

## 📌 Overview
An autonomous mobile robot designed for warehouse automation. It features **SLAM-based navigation**, obstacle avoidance, and a **Python-controlled prismatic tray** to deliver inventory to specific vertical heights.



## 🛠️ Key Technologies
* **SLAM:** GMapping/Cartographer for real-time occupancy grid mapping.
* **Sensor Fusion:** Extended Kalman Filter (EKF) via `robot_localization` package.
* **Actuation:** Prismatic joint URDF with Python-based position control.
* **Navigation:** ROS Navigation Stack (MoveBase) for global and local path planning.

## 📂 Project Structure
* `/urdf`: Robot model with LiDAR, Camera, and Tray joints.
* `/scripts`: Python nodes for navigation and tray control.
* `/launch`: Files to initialize Gazebo, RViz, and EKF nodes.

## 🎮 Usage
1. **Launch Environment:**
   `roslaunch inventory_bot warehouse.launch`
2. **Set Initial Pose:**
   `python3 set_initial_pose.py`
3. **Move to Target:**
   `python3 move_bot.py <x> <y>`
4. **Actuate Tray:**
   `python3 move_tray.py <height_in_meters>`



---
**Author:** Jomon George Reji | MSc Mechatronics & Cyber Physical Systems
