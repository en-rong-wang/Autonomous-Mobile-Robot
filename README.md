# Autonomous-Mobile-Robot
Developed a ROS 2-based autonomous mobile robot integrating LiDAR-based mapping, localization, path planning, obstacle avoidance, and real-time object tracking using YOLOv26 and an Intel RealSense depth camera on NVIDIA Jetson Nano.
## LiDAR-Based Indoor Navigation with ROS 2 Nav2

<table>
  <tr>
    <td align="center" width="50%">
      <img src="lidar_map.jpg" width="300">
    </td>
    <td align="center" width="50%">
      <img src="costmap.jpg" width="300">
    </td>
  </tr>
  <tr>
    <td valign="top">
      <b>2D LiDAR Mapping with GMapping SLAM</b>
      <br><br>
      Mapped a basement with an N10P 2D LiDAR and GMapping SLAM, then saved the occupancy grid as a PGM image for robot localization and navigation.
    </td>
    <td valign="top">
      <b>ROS 2 Nav2 Costmap and Navigation Tuning</b>
      <br><br>
      Nav2 costmap visualization showing inflated cost regions around obstacles. I used YAML configuration files to tune the costmap’s inflation radius, set velocity and acceleration limits, and adjust goal tolerances.
    </td>
  </tr>
</table>


A mobile robot navigates a LiDAR-mapped basement using ROS 2 Nav2, with A* for global route planning and DWA for local obstacle avoidance.

https://github.com/user-attachments/assets/1f985da0-408c-414a-a2d3-f6f2ff451f1c



## Tennis Ball Detection and Tracking on NVIDIA Jetson Nano

Developed an onboard tennis ball tracking system for a mobile robot using an Intel RealSense depth camera and YOLOv26.

- Annotated tennis ball images in Roboflow and used the resulting dataset to obtain custom YOLOv26 model weights.
- Implemented the detection and tracking pipeline in PyTorch and deployed it on an NVIDIA Jetson Nano with CUDA-accelerated inference.
- Combined YOLO detections with RealSense depth measurements to track the ball’s position and estimate its distance from the camera. Detection confidence reached up to 97% during testing.

### Experimental Demonstration

https://github.com/user-attachments/assets/73689d51-dcad-4e06-a631-b5118f9bbd1f

