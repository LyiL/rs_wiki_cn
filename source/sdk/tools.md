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