# 测试框架

## 测试层级

```
tests/
├── unit/           # 单元测试 - 函数级别
├── integration/    # 集成测试 - 模块交互
├── hil/            # HIL测试 - 硬件在环
└── conftest.py     # pytest 公共配置
```

## CI 集成

测试在 CI 中自动执行，参见 [.github/workflows/ci.yml](../../.github/workflows/ci.yml)

| 阶段 | 触发条件 | 测试范围 |
|------|---------|---------|
| PR检查 | 每次PR | unit + integration |
| 主分支 | merge到main | 全部 |
| 发布 | tag推送 | 全部 + 构建产物 |

## 本地运行

```bash
# 单元测试
pytest tests/unit/ -v

# 集成测试
pytest tests/integration/ -v

# 全部测试 + 覆盖率
pytest tests/ --cov=implementation/
```

## 命名规范

- 测试文件: `test_*.py`
- 测试函数: `test_<功能描述>`
- 测试类: `Test<模块名>`
