# 工具  
## 采集  
基于 ros2 开发的超级传感器采集软件包，并通过参数配置方式实现不同节点数据采集功能，采集的数据格式根据采集配置不同，支持.db3和.mcap两种格式。  
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/sdk_infra/-/blob/main/modules/ros2_collect/README_zh.md)  

## 监控  
监控 ros2 中关心的一些指标，例如: 内存/CPU/IO使用率、消息帧率、消息时间戳与当前系统时间的差值等，监控结果会通过日志和 topic 输出。同时，该软件包还提供了将监控结果数据生成可视化报告的 python 脚本，可以本地生成包含简易统计结果以及折线图的 html 格式报告。  
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/rs_monitor/-/blob/main/README_cn.md)  

## 标定  
**相机内参标定**  
针孔相机会使图像产生严重的畸变，主要的畸变类型包括径向畸变和切向畸变。本模块根据张正友标定法原理提供相机内参标定工具。开发者可根据工具指引，在不同角度拍摄靶板（可利用本模块中提供的示例图案进行制作）进行相机标定，以提供其他模块所需要的相机内参与畸变系数。  
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/calibration/-/blob/main/README_CN.md)   

**相机到雷达的标定**  
本模块提供相机-雷达标定工具，复用相机内参标定靶板，对相机与雷达分别进行靶板位姿估计，以提供其他模块所需要相机-雷达外参。标定时请确保靶板处于图像与点云的FOV之内，并尽量保持AC1稳定，避免因为传感器抖动引入标定误差。  
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/calibration/-/blob/main/README_CN.md)   

**AC1 传感器到移动轮式平台外参标定**  
本模块提供AC1-移动轮式平台外参标定（角度标定）。本模块需提前录制两段数据：一段沿着直线匀速行驶的数据、一段绕固定轴匀速旋转的数据。开发者按照工具操作指引，启动工程后依次播放这两段数据，完成标定后输出传感器到移动轮式平台的角度外参，平移部分需开发者进行测量后，填入标定文件。  
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/calibration_extrinsic/-/blob/main/README_CN.md)   

## 交叉编译  
该工具用于管理 Super Sensor SDK 的跨平台编译和本地编译环境的 Docker 容器。包含了容器管理、镜像管理以及自动化环境设置等功能。    
[点击了解详情](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/sdk_infra/-/blob/main/tools/cross_compilation/README_zh.md)  