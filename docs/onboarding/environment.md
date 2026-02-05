# 开发环境配置

## 必需工具

### 通用工具
| 工具 | 用途 | 安装 |
|------|------|------|
| Git | 版本控制 | `winget install Git.Git` |
| VSCode | 代码编辑 | `winget install Microsoft.VisualStudioCode` |
| Python 3.10+ | 仿真脚本 | `winget install Python.Python.3.10` |

### 理论组
| 工具 | 用途 |
|------|------|
| MATLAB/Simulink | 建模仿真 |
| NumPy/SciPy | Python科学计算 |

### 实装组
| 工具 | 用途 |
|------|------|
| ARM GCC | 交叉编译 |
| OpenOCD / J-Link | 调试烧录 |
| STM32CubeMX | 配置工具 |

## 环境配置步骤

### 1. 克隆仓库
```bash
git clone <repo-url>
cd drone-flight-lab
```

### 2. Python 环境
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

### 3. 验证安装
```bash
python --version
git --version
```

## VSCode 推荐扩展

- C/C++ (ms-vscode.cpptools)
- Python (ms-python.python)
- GitLens (eamodio.gitlens)
- Cortex-Debug (marus25.cortex-debug)

## 常见问题

**Q: Python虚拟环境激活失败？**
A: PowerShell 执行 `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

**Q: Git 中文乱码？**
A: `git config --global core.quotepath false`
