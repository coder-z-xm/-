# CLAUDE.md — 拾记·笔记管理系统

面向 Claude Code 的项目级说明。**先读 `指令集/fast.md`**——本项目协作规则以 `指令集/` 为准，本文件只做「桥接 + 补充边界」，不与指令集重复。

## 项目是什么
- 拾记·笔记管理系统：uni-app（Vue 3）+ uniCloud（支付宝云 `uniCloud-alipay`），目标平台 H5。
- 课程期末大作业，多人协作。前端目前读 `src/data/demo.js` 演示数据；登录、真实 CRUD、文件上传、发布均未接入。

## 每次任务必读的协作文档
- `指令集/fast.md` —— 关键词 `UP` / `AILOG` / `PUSH` / `PRB` / `GIT` 的定义与执行顺序（`UP → PUSH → PRB → GIT`）。
- `指令集/log.md` —— **唯一的修改日志**（不要再建 CHANGELOG.md）。
- `指令集/stage.md` —— 阶段清单。
- `指令集/problem.md` —— 问题记录。
- `AI_details/AI_LOG.md` —— 作业要求的 AI 使用日志（六要素），由 `UP` / `AILOG` 维护。

## 修改日志
- 每次实际改动后按 `UP` 约定更新 `指令集/log.md`：顶部新增一条（时间戳 / 修改概括 / 涉及文件 / 代码部分 / 思路与决策）。
- 只记录必要信息，不整段复制代码或提示词原文。

## 编辑路线（路线 A：agent 改代码，HBuilderX 只运行）
- agent 直接修改代码文件；不在 HBuilderX 里手改代码。
- HBuilderX 只用于「运行到浏览器 / 真机调试 / 发布」。

## 高风险文件（改动前先 diff，未经确认不覆盖）
- `manifest.json` —— 含 appid 与云端关联配置，HBuilderX 会回写，谨防丢失。
- `pages.json` —— 页面路由与 tabBar。
- `uni_modules/**` —— 第三方插件，勿手改。
- `uniCloud-alipay/database/*.schema.json` —— 数据库结构，线上变更需谨慎。

## 部署边界（重要）
- 云函数 / schema 的「上传部署」、发布、任何可能计费的操作，**默认由用户在 HBuilderX 里执行**，agent 不擅自部署。
- agent 只负责：改代码文件、commit、更新日志。

## git 约定
- 只有用户明确指示或 `GIT` 关键词时才 `commit` / `push`；其余关键词不碰 git。
- push 前先 `git fetch`，发现冲突立即停下询问，**禁止 force push**。
- 不提交：`unpackage/`、`.hbuilderx/`、`node_modules/`、`.env`、密钥。

## 当前状态
- 阶段 1（前端页面框架）已完成，多数交互为占位；阶段 2（uniCloud 服务空间接入）未开始。

## 作业硬性要求（期末大作业 2026）
- 必须提交 `AI_details/AI_LOG.md`，逐条记录六要素：任务 → 用的工具 → 提示要点 → AI 给出的方案 → 哪里错了 / 哪里不可靠 → 最终怎么改。
- 最终打包四项：演示文稿 PPT + 完整源码 + 项目报告 PDF + AI-Log；截止 2027-01-03。
- 严禁提交自己看不懂的代码；AI_LOG 条目提交前须由组员核对。
