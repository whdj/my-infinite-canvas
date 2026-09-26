# My Infinite Canvas

My Infinite Canvas 是一个本地优先的 AI 创作工作台，把无限画布、提示词、素材、模型调用和 Agent 工作流放在同一个界面里。

## 功能

- 无限画布：多画布项目、节点拖拽缩放、连线、小地图、撤销重做、复制粘贴、导入导出。
- AI 创作：兼容 OpenAI 协议的文本、图片、参考图编辑、视频和音频接口。
- 工作流节点：文本、图片、视频、音频和生成配置节点可以连接成连续流程。
- 提示词中心：内置来源、自定义 JSON 来源、搜索、标签筛选和本地缓存。
- 我的资产：在浏览器本地保存图片、视频、音频和可复用提示词。
- 本地 Agent：通过 Canvas Agent、Codex 和 MCP 连接本机工作流。
- 插件系统：支持远程插件和 TypeScript 节点 SDK。
- 数据同步：支持 WebDAV 同步画布、资产和生成记录。

## 本地运行

```bash
cd web
npm install --legacy-peer-deps
npm run dev
```

打开 `http://localhost:3000`，在右上角配置 OpenAI 兼容接口的 Base URL、API Key 和模型名称。

Windows 下如果 npm 没有安装可选原生依赖，可以执行：

```bash
npm install --legacy-peer-deps @rollup/rollup-win32-x64-msvc lightningcss-win32-x64-msvc @tailwindcss/oxide-win32-x64-msvc
```

## Docker

```bash
docker compose up -d
```

默认访问 `http://localhost:3000`。

## 本地 Agent

```bash
npm --prefix canvas-agent install
npm --prefix canvas-agent run dev
```

启动后，把终端输出的 Local URL 和 Connect token 填入网页右上角的 Agent 面板。

## 数据和安全

API Key、画布、素材和生成记录默认保存在浏览器本地。AI 请求由浏览器直接发送到你配置的接口；不要把 API Key 提交到 Git。

本项目保留原始 MIT 许可证及其版权声明，详见 [LICENSE](LICENSE)。
