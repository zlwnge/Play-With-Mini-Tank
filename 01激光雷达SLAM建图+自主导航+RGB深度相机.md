设备：wheeltec的mini-tank，配备思岚A1

## 激光SLAM建图
- 小车开机，连接WiFi
- SSH远程登录
- 启动激光SLAM建图，在第一个终端运行`mapping.launch`文件
- 查看建图效果`rviz`
- 建图完成保存地图`map_saver.launch`
> 保存地图时使用的终端需要登录到小车。不然会报错
> 运行`mapping.launch`文件前，需要看看其中的默认参数是否与设备对应，否则会出现各种错误，比如地图加载不出来

## 自主导航
- 小车开机，连接WiFi
- SSH远程登录
- 在终端运行`navigation.launch`文件
- 打开rviz，使用2D Pose Estimate调整小车姿态，使用2D Nav Goal设定小车目标点的位置

## 查看RGB和深度相机
- 运行`usb_cam`包中的`usb_cam_test.launch`文件
- rviz中添加`image`及相应话题

- 运行`astra_camera`包中的`astra.launch`文件
- rviz中添加`image`及相应话题
