# 驱动
## Driver  
Driver 是 Robosense 机器人传感器产品的驱动。它基于 C/C++ 语言开发，为用户提供了易用的 C/C++语言风格的接口。通过该 Driver，用户可以快速地连接 Robosense 机器人传感器并接收点云数据。详情及安装和使用方法见

## ROS Driver  

## ROS2 Driver  
ROS2 driver是一个全新的 ROS2 包，专门用于连接 Robosense 生产的机器人传感器产品。该驱动程序可以在安装了 ROS2 环境（indigo,kinetic,melodic）的 ubuntu14.04/16.04/18.04，Windows，Mac 等操作系统下运行。详情及安装和使用方法见  


# 时间同步  
**PTP：** IEEE 1588v2.0 PTP 网络协议同步  

**GPS：** 秒脉冲 + GPRMC 时间数据，组成 GPS 时间同步方式  

**PPS：** 秒脉冲同步，需要上层应用程序通过其他途径（如：uart）获取每个脉冲的时间信息，并修正点云时间。目前仅 LiDAR 支持这种同步方式，且由于用法较为复杂，不推荐用户使用这种方式进行 LiDAR 时间的同步  


# 工具  
## 采集  
基于 ros2 开发的超级传感器采集软件包，并通过参数配置方式实现不同节点数据采集功能，采集的数据格式根据采集配置不同，支持.db3和.mcap两种格式。  
[点击了解详情](http://10.10.0.20/super_sensor_sdk/ros2_sdk/sdk_infra/-/blob/main/modules/ros2_collect/README_zh.md)  

## 监控  
监控 ros2 中关心的一些指标，例如: 内存/CPU/IO使用率、消息帧率、消息时间戳与当前系统时间的差值等，监控结果会通过日志和 topic 输出。同时，该软件包还提供了将监控结果数据生成可视化报告的 python 脚本，可以本地生成包含简易统计结果以及折线图的 html 格式报告。  
[点击了解详情](http://10.10.0.20/super_sensor_sdk/ros2_sdk/rs_monitor/-/blob/main/README_cn.md)  

## 标定  

## 交叉编译  
该工具用于管理 Super Sensor SDK 的跨平台编译和本地编译环境的 Docker 容器。包含了容器管理、镜像管理以及自动化环境设置等功能。    
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/sdk_infra/-/blob/main/tools/cross_compilation/README_zh.md)  


# 定位  
**localization** 用于提供实时的相对定位信息或全局定位信息,该项目包含了以下两个模块：  
- msf_localization 是基于 ESKF 框架的融合定位模块，可提供只基于 imu+轮速 的相对定位信息以及融合 点云定位结果 的全局定位信息，该模块也可接入其他传感器观测进行后续拓展；
- lidar_localization 是基于点云地图的点云定位模块，使用 ceres 进行优化，使用 pcl 进行点云处理。  
[点击了解详情](http://10.10.0.20/super_sensor_sdk/ros2_sdk/localization/-/blob/main/README_zh.md) 

# SLAM  
一个融合 LiDAR、视觉和 IMU 等多传感器紧耦合里程计系统。基于 HKU-MARS 实验室开源的 FAST-LIVO 工程开发，针对 Active Camera 进行专门的适配和优化，能够实时输出 Active Camera 的姿态，并生成带颜色信息的三维点云。  
<iframe width="100%" height="315" src="https://cdn.robosense.cn/EM4/%E5%8F%91%E5%B8%83%E4%BC%9A%E5%9B%9E%E9%A1%BE.mp4" frameborder="0" allowfullscreen></iframe>  
<iframe width="100%" height="315" src="https://cdn.robosense.cn/EM4/%E5%8F%91%E5%B8%83%E4%BC%9A%E5%9B%9E%E9%A1%BE.mp4" frameborder="0" allowfullscreen></iframe>  


# 目标检测与识别  
通过 Yolov8 检测模型对图像中的主要障碍物（例如人、车等）进行识别，得到目标的类别与位置  

[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/perception) 


# 语义分割  
通过 模型对图像进行语义分割，生成目标的分割掩码  

[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/perception) 

# 点云与视觉融合  
利用传感器自带IMU进行运动补偿，并将图像和点云相互映射，进行可视化  

[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/postprocess) 