# 目标检测与识别  
通过 Yolov8 检测模型对图像中的主要障碍物（例如人、车等）进行识别，得到目标的类别与位置。  

以下视频提供了速腾前台的行人检测离线演示效果，主要使用的硬件配置为  
<div class="wy-table-responsive">
    <table class="docutils align-default">
        <tbody>
            <tr class="row-even">
                <td>计算平台</td>
                <td>CPU: Intel® Core™ i7-11700 @ 2.50GHz × 16 <br> GPU: NVIDIA GeForce RTX 3060 <br> MEM: 32GB </td>
            </tr>
            <tr class="row-odd">
                <td>传感器</td>
                <td>AC1</td>
            </tr>
        </tbody>
    </table>
</div> 
<iframe width="100%" height="389" src="https://cdn.robosense.cn/AC1target_detection.mp4" frameborder="0" allowfullscreen></iframe>  

视频数据：  

详细代码：[AC1 Pedestrian Detection](http://gitlab.robosense.cn/super_sensor_sdk/ros2_sdk/perception) 