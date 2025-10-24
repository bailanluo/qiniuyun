# Agent 智能客服系统

这是一个基于 AI 的智能客服系统，包含后端 API 服务和前端控制界面。

## 项目结构

```
qiniu/
├── Agent/              # 后端项目 (FastAPI)
│   ├── app/           # 应用核心代码
│   ├── tests/         # 测试文件
│   ├── docs/          # 项目文档
│   └── .git/          # 后端独立 Git 仓库
├── Agent_control/      # 前端项目 (Vue.js)
│   ├── src/           # 前端源码
│   ├── public/        # 静态资源
│   └── .git/          # 前端独立 Git 仓库
└── .git/              # 总项目 Git 仓库
```

## 开发说明

### 后端开发
```bash
cd Agent
# 安装依赖
pip install -r requirements.txt
# 启动服务
python -m uvicorn app.main:app --reload
```

### 前端开发
```bash
cd Agent_control
# 安装依赖
npm install
# 启动开发服务器
npm run dev
```

## Git 管理

- **总仓库**: 管理整个项目的文档和配置
- **后端仓库**: 独立管理后端代码和 API
- **前端仓库**: 独立管理前端界面和组件

每个子项目都有独立的 Git 仓库，可以独立开发、部署和版本管理。

## 技术栈

- **后端**: FastAPI + Python
- **前端**: Vue.js + TypeScript
- **数据库**: MySQL
- **AI 模型**: 支持多种 LLM 接口
