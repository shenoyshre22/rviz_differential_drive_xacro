# rviz_differential_drive_xacro
A ROS 2 Jazzy package utilizing Xacro templates to design, configure, and visualize a differential drive mobile robot in RViz
---

##  Terminal Commands to Run:

1. Environment Setup:
   ```bash
   # Append local binary tool routings
   export PATH=$PATH:~/.local/bin

   # Source core ROS 2 installation configurations
   source /opt/ros/jazzy/setup.bash
   ```
2. Building the Workspace
    ```bash
    # Navigate to the workspace root directory
    cd ~/ros2_ws

    # Force clean old environment build   paths
    rm -rf build/xx_robot_description install/xx_robot_description

    # Build the specific package configurations using symlink rules
    colcon build --packages-select xx_robot_description --symlink-install

    # Source your updated local environment overlay definitions
    source install/setup.bash
    ```
3. Launching in RViz
   ```bash
   # Clear out any lingering visualization server tasks
    pkill -f robot_state_publisher
    pkill -f rviz2

    # Execute the launcher using the direct Xacro package source file
    ros2 launch urdf_tutorial display.launch.py model:=/home/arc/ros2_ws/src/xx_robot_description/urdf/xx_robot.xacro
   ```
---
 ## Final Robot from all angles:
<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/19dfc69c-644f-4b53-8162-50efbe09a88e" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/f48b523b-3cd5-4d07-a962-909c406ac872" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/eca73a38-b550-479a-b844-1854ee8bbdfd" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/48ca85ef-03b8-431c-aced-4313b4063956" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/3e2524a6-6cfb-476c-954f-f32bb59813e6" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/c9b39942-48d4-4e1d-b20b-8f85b7b3a117" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/77802d7c-578c-432e-9304-110706278148" />

<img width="1292" height="759" alt="image" src="https://github.com/user-attachments/assets/9a718d88-ee3b-47fe-8406-53e087a8ebd7" />
