# ROS Qt Demo

## 说明

本项目暂时只适用于 ROS Noetic 版本。

## 功能包介绍

本功能包是实现 ROS1 移动机器人人机交互软件的基础模板。

## 功能包结构

```
ros_qt_demo
├── CMakeLists.txt
├── include
│   ├── ros_qt_demo
│   │   ├── main_window.hpp
│   │   ├── qnode.hpp
│   └── ros_qt_demo_msgs
│       ├── msg
│       │   └── msg1.msg
│       └── srv
│           └── srv1.srv
├── launch
│   └── demo.launch
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
├── ui
│   └── main_window.ui
└── urdf
    └── my_robot.urdf
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

## 运行功能包

在终端中输入以下命令进行运行：

```bash
    roslaunch ros_qt_demo demo.launch
```
