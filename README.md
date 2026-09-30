# Zekeep_control_py

Zekeep 六轴机械臂使用的 Python 控制 SDK。此仓库保留与现有 ROS、MoveIt 和视觉工具兼容的 `reBotArm_control_py` Python 导入名；仓库名用于区分 Zekeep 维护的配置与修改版。

## 能力

- 电机通信与状态读取。
- 六轴正逆运动学、末端控制和轨迹规划。
- Pinocchio 动力学与重力补偿。
- DM、RS 电机配置及机械臂 URDF。

## 安装

在 Ubuntu 22.04、Python 3.10 环境中先准备 Pinocchio、MotorBridge 和其他依赖，再安装本地包：

```bash
python -m pip install --no-deps -e .
```

此安装命令只安装 Python SDK，不会连接机械臂或使能电机。使用硬件前检查串口、机械臂型号和控制参数；不要让本 SDK 与 ROS 驱动同时占用同一控制接口。
