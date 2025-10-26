# Agent 智能客服系统

这是一个基于 AI 的智能客服系统，包含后端 API 服务和前端控制界面。

## 环境要求

- **Python**: 3.9+
- **Node.js**: ^20.19.0 || >=22.12.0
- **MySQL**: 8.0+

## 快速开始

### 1. 后端部署

```bash
# 进入后端目录
cd Agent

# 安装依赖
pip install -r requirements.txt

# 配置环境变量（复制示例文件并修改）
cp .env.example .env

# 启动服务（方式一：使用启动脚本）
python scripts/start_server.py

# 或（方式二：直接启动）
python -m uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

后端服务默认运行在：http://localhost:8000

### 2. 前端部署

```bash
# 进入前端目录
cd Agent_control

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

前端服务默认运行在：http://localhost:5173

## 项目结构

```
qiniu/
├── Agent/              # 后端项目 (FastAPI)
│   ├── app/           # 应用核心代码
│   ├── config/        # 配置文件
│   └── scripts/       # 启动脚本
└── Agent_control/      # 前端项目 (Vue.js)
    ├── src/           # 前端源码
    └── public/        # 静态资源
```

## 技术栈

- **后端**: FastAPI + Python + MySQL
- **前端**: Vue.js + TypeScript + Vite
- **AI**: LangChain + LangGraph

## Git 仓库

本项目使用**三个独立的 Git 仓库**管理：

- **总项目仓库**: [qiniuyun](https://github.com/bailanluo/qiniuyun) - 包含项目文档和整体说明
- **后端仓库**: [agent](https://github.com/bailanluo/agent) - 包含 FastAPI 后端代码
- **前端仓库**: [agent_control](https://github.com/bailanluo/agent_control) - 包含 Vue.js 前端代码
