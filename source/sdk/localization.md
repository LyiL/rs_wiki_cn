# 定位  
**localization** 用于提供实时的相对定位信息或全局定位信息，该项目包含了以下两个模块： 
- msf_localization 是基于 **ESKF** 框架的融合定位模块，可提供只基于 **imu+轮速** 的相对定位信息以及融合 **点云定位结果** 的全局定位信息，该模块也可接入其他传感器观测进行后续拓展；
- lidar_localization 是基于点云地图的点云定位模块，使用 ceres 进行点云匹配，使用PCL进行点云预处理。  

[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/localization/-/blob/main/README_zh.md)   

Demo数据下载地址：[点击下载](https://cdn.robosense.cn/AC1localization_demo.zip)  