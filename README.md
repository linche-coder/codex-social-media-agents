# 紫宸星宇社媒 Agent

面向 Codex 的社媒工具合集。此仓库同时提供两个可独立安装的技能插件：

- **社媒自动发布 Agent**：批量发布视频和图文，支持 AI 文案、立即发布和多时间定时发布。
- **社媒互动 Agent**：单平台浏览推荐内容或关键词搜索结果，并准备点赞、评论、收藏、关注和已有私信回复。

## 安装方式

### 团队工作区安装

由工作区管理员操作：

1. 打开 **Admin → Plugins**。
2. 选择 **Add → Import marketplace**。
3. 仓库地址填写 `https://github.com/linche-coder/codex-social-media-agents`。
4. 本仓库的市场文件位于根目录，`Path` 保持为空。
5. 导入完成后，成员可在插件目录中分别安装两个 Agent。

私有仓库需要先向团队成员和工作区使用的 GitHub 连接授予读取权限。

### 本地测试安装

克隆仓库后，在仓库根目录执行：

```text
codex plugin marketplace add .
codex plugin add social-media-publisher@zichen-social-agents
codex plugin add social-media-interaction-agent@zichen-social-agents
```

安装或更新后，请新建一个 Codex 任务进行测试。

## 快速使用

### 社媒自动发布 Agent

```text
使用 $media-publish 发布视频或图文，请先给我一份可复制填写的任务模板。
```

### 社媒互动 Agent

```text
使用 $social-media-interact，选择小红书，通过关键词“露营装备”搜索内容：
浏览 20 条，点赞最多 5 条，评论最多 3 条，收藏最多 2 条，关注最多 1 个账号，不回复私信。
```

## 使用前准备

- 使用支持插件和内置浏览器的 Codex。
- 每位用户都需要在自己的 Codex 内置浏览器中登录目标平台。
- 插件不包含账号密码、Cookie、Token 或其他用户凭证。
- 发布或互动前应检查最终对象、文案、数量和时间。
- 平台页面结构、账号权限和风控规则可能变化，实际能力以运行时页面为准。

## 使用说明

- [社媒自动发布 Agent 使用说明](docs/紫宸星宇效能部_社媒自动发布Agent使用说明_V1_0.pdf)
- [社媒互动 Agent 使用说明](docs/紫宸星宇效能部_社媒互动Agent使用说明_V1_0.pdf)

## 目录结构

```text
.
├── .agents/plugins/marketplace.json
├── plugins/
│   ├── social-media-publisher/
│   └── social-media-interaction-agent/
├── docs/
└── README.md
```

维护方：紫宸星宇效能部
