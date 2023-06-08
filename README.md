# MultiSensorsCalibration
it is a conclusion of several ways to make calibration for multi-sensors
## 雷达-IMU标定方案
1. 苏黎世理工开源方案：\
  个人评价：本来是针对odmetry和lidar的标定修改后可用于IMU标定，不是针对IMU设计的，标定精度不容易提升\
  链接地址：https://github.com/ethz-asl/lidar_align \
  数据要求：基于rosbag的消息\
  数据采集的要求：

2. 浙大LI-Calib
  个人评价：最靠谱的一个 \
  链接地址：https://github.com/APRIL-ZJU/lidar_IMU_calib \
  数据要求：rosbag velodyne_packets原始数据 \
  数据采集要求：平面多，1m范围内z轴动态，30s左右即可

3. lidar_imu_calib
 个人评价：只能用来标定旋转量，不能标定平移量，速度较快 \
 链接地址：https://github.com/chennuo0125-HIT/lidar_imu_calib \
 数据要求：rosbag topic为sensormessage数据\
 数据采集：一分钟左右的数据，动态

4. SensorsCalibration
 个人评价：包含多个不同组合传感器标定，激光IMU标定需要有GPS，纯IMU激光不可用。\
 链接地址：https://github.com/PJLab-ADG/SensorsCalibration \
 数据要求：8字型55X15范围的移动，平坦路面，静态物体 \

5. kalibr工具箱
 个人评价：具有相机IMU标定功能，无lidar-imu标定 \
 链接地址：https://github.com/ethz-asl/kalibr

