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

## 来源与命名

此公开仓库由 [Seeed-Projects/reBotArm_control_py](https://github.com/Seeed-Projects/reBotArm_control_py) fork，包含 Zekeep 使用的配置和代码修改。上游仓库未声明明确的开源许可证；本仓库保留 fork 关系与上游历史，不添加新的上游代码许可。请查看上游仓库及其维护者说明，再决定如何复制、再发布或用于其他项目。

Python 模块名仍为 `reBotArm_control_py`，以保持 Zekeeparm 工作区现有导入路径兼容。
