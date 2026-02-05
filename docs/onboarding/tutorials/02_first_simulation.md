# 教程 02: 第一个仿真

## 学习目标

运行一个简单的四旋翼仿真，理解基本工作流程。

## 前置条件

- 已完成环境配置
- Python 虚拟环境已激活

## 步骤

### 1. 进入仿真目录

```bash
cd theory/simulation
```

### 2. 运行示例（待添加）

```bash
python sim_hover.py
```

### 3. 观察输出

仿真将展示:
- 姿态响应曲线
- 高度控制效果
- 电机输出

## 练习

1. 修改初始姿态，观察响应变化
2. 调整控制器参数，对比效果
3. 尝试添加外部扰动

## 代码结构说明

```python
# sim_hover.py 基本结构（示例）

# 1. 参数定义
params = {...}

# 2. 初始化状态
state = init_state()

# 3. 仿真循环
for t in time:
    sensor = read_sensors(state)
    control = controller(sensor, target)
    state = dynamics(state, control)

# 4. 结果可视化
plot_results()
```

## 下一步

继续 [03_dynamics_basics.md](03_dynamics_basics.md) 学习动力学基础
