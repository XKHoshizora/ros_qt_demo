# ROS Qt Demo

## 说明

本项目暂时只适用于 ROS Noetic 版本。

## 功能包介绍

本功能包是以 Qt5 为基础实现的 ROS1 移动机器人人机交互软件的基础模板。

## 功能包结构

```
ros_qt_demo
├── CMakeLists.txt
├── include
│   └── ros_qt_demo
│       ├── main_window.hpp
│       └── qnode.hpp
├── mainpage.dox
├── package.xml
├── resources
│   ├── images
│   │   └── icon.png
│   └── images.qrc
├── src
│   ├── main_window.cpp
│   ├── main.cpp
│   └── qnode.cpp
└── ui
    └── main_window.ui
```

## 下载此功能包

下载本项目的压缩包，或使用以下命令克隆本包到自己工作空间的 `src` 目录下：

```bash
cd ~/<catkin>_ws/src
git clone https://github.com/XKHoshizora/ros_qt_demo.git
```

## 更改功能包名称

如果需要更改功能包的名称，请按照以下步骤进行更改:

1. 使用文本编辑器打开`cmakelist.txt` 文件，并利用查找与替换功能将 `ros_qt_demo` 替换为自己想要的名称。
   ![image.png](https://i.postimg.cc/zfZ1s8RB/image.png)

2. 使用文本编辑器打开 `package.xml` 文件，并利用查找与替换功能将 `ros_qt_demo` 替换为自己想要的名称。

3. 找到 `include` 目录下两个 `hpp` 文件中含有 `ros_qt_demo` 的部分（如： `#include "../include/ros_qt_demo/..."`，`namespace class1_ros_qt_demo` .etc），并将其中的 `ros_qt_demo` 部分替换为自己的功能包名称。

4. 找到 `src` 目录下三个 `cpp` 文件中含有 `ros_qt_demo` 的部分（如： `#include "../include/ros_qt_demo/..."`，`namespace class1_ros_qt_demo` .etc），并将其中的 `ros_qt_demo` 部分替换为自己的功能包名称。
   ![image.png](https://i.postimg.cc/8ch8qT6D/image.png)

## 编译功能包

在终端中输入以下命令进行编译：

```bash
cd ~/catkin_ws
catkin_make
```

## 刷新终端

在终端中输入以下命令进行刷新：

```bash
source ./devel/setup.bash
```

## 运行功能包

在终端中输入以下命令进行运行：

```bash
rosrun ros_qt_demo ros_qt_demo
```

## 测试

打开一个新的终端，输入以下命令打开 ROS Master：

```bash
roscore
```

在刚刚的图形界面中找到 `Use environment variables` 选项并打勾，再点击下面的 `Connect` 按钮，点击即可创建一个发布节点。

再次打开一个新的终端，输入以下命令查看发布中的话题：

```bash
rostopic list
```

可以看到一个名为 `/chatter` 的话题。

在该终端中输入以下命令，可查看发布中的消息：

```bash
rostopic echo /chatter
```

## 参考

[ROS Qt5 librviz 人机交互界面开发一（配置 QT 环境）](https://blog.csdn.net/qq_38441692/article/details/105158790)
