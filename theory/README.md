# Theory - 数学与物理模型研发

## 目录结构

```
theory/
├── dynamics/      # 动力学模型
├── control/       # 控制算法
├── simulation/    # 仿真环境
└── docs/          # 理论文档
```

## 研发流程

1. **建模** → dynamics/
2. **控制设计** → control/
3. **仿真验证** → simulation/
4. **交付实装** → 输出至 implementation/

## 文件命名规范

- 公式推导: `*_derivation.md`
- 算法设计: `*_algorithm.md`
- 仿真脚本: `sim_*.py` 或 `sim_*.m`
