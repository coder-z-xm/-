# AI 使用日志 · AI_LOG.md

> 作业要求（见《期末大作业 2026》）：必须提交 `AI_LOG.md`，逐条记录
> **任务 → 用的工具 → 提示要点 → AI 给出的方案 → 哪里错了 / 哪里不可靠 → 最终怎么改**。
>
> - 本文件是最终提交的四项材料之一（AI-Log），提交前**必须由组员逐条核对**。
> - 文件位置：项目根目录 `AI_details/`；维护方式：`UP` 会自动追加，单独补录使用 `AILOG`（见 `../指令集/fast.md`）。
> - 下方条目为根据当前会话整理的草稿，工具 / 提示 / 结论与实际不符处请直接修改。

## 记录规范

- 六要素顺序固定，缺一不可；「哪里错了 / 哪里不可靠」不能省略，没有明显错误时也要写可靠性评估。
- 不复制大段提示词原文，只写要点；不提交自己看不懂的代码。
- 多人协作时注明记录人与涉及文件，便于答辩时定位。
- 组员使用其他 AI 工具（ChatGPT、DeepSeek、Copilot 等）的记录需自行补充，不要只写 Claude。

## 模板

```markdown
## YYYY-MM-DD HH:mm ｜ 任务：……

- **任务**：
- **用的工具**：
- **提示要点**：
- **AI 给出的方案**：
- **哪里错了 / 哪里不可靠**：
- **最终怎么改**：
- **涉及文件**：
- **记录人**：
```

---

## 2026-11-25 22:10 ｜ 任务：把本地项目与 GitHub 仓库对齐

- **任务**：将 `C:\Users\15704\Desktop\zhixu\zhixuLink` 与仓库 `coder-z-xm/-` 的 `ZHIXU/` 目录内容对齐。
- **用的工具**：Claude Code
- **提示要点**：提供仓库链接，要求把本地文件夹下的项目与仓库里的内容对齐。
- **AI 给出的方案**：临时 clone 仓库，逐文件 diff；以仓库版本为准覆盖本地脚手架，保留本地独有的配置文件与空的云函数目录；同步后备份再删除。
- **哪里错了 / 哪里不可靠**：AI 初版方案直接整体复制，未先评估 `manifest.json` 的差异，导致本地真实 appid 与完整打包配置被仓库的占位精简版覆盖，后续才需要二次合并；「本地只是空脚手架」这一判断依赖人工 diff，不是自动校验。
- **最终怎么改**：先 clone 并逐文件比对，确认仓库为更完整版本后再复制；保留 `.editorconfig`、`.gitignore`、空 `cloudfunctions/`；发现 manifest 问题后单独合并恢复 appid 与打包配置，并做最终一致性比对。
- **涉及文件**：`App.vue`、`main.js`、`pages.json`、`manifest.json`、`index.html`、`uni.scss`、`pages/*`、`src/data/demo.js`、`static/*`、`uniCloud-alipay/database/notes.schema.json`、`uni_modules/*`
- **记录人**：待补充

---

## 2026-11-25 22:20 ｜ 任务：合并 appid 并初始化 git 远端

- **任务**：删除同步前备份；把真实 appid 与完整打包配置合并回新 manifest；初始化 git 仓库并添加 GitHub remote。
- **用的工具**：Claude Code
- **提示要点**：删除指定备份目录；实现此前提出的两点（恢复 appid / 初始化 git + remote，不自动提交推送）。
- **AI 给出的方案**：从备份恢复完整 manifest，合并仓库的元信息；`git init -b main`、添加 origin、fetch 后跟踪 `origin/main`。
- **哪里错了 / 哪里不可靠**：AI 没有先确认仓库根目录结构（实际是 `LICENSE + ZHIXU/`），就把本地项目根当成仓库根直接对齐；`git reset origin/main` 后工作区显示 `LICENSE`、`ZHIXU/*` 全部被删除，属于误导状态；GitHub 网络多次超时，fetch 并非一次成功，方案对网络稳定性过于乐观。
- **最终怎么改**：撤销本地分支与索引映射，回退为空仓库（无提交、无推送），保留 `origin/main` 引用；把「本地根 vs 仓库子目录」登记为问题 P1，等确认同步方案；manifest 合并结果保留。
- **涉及文件**：`manifest.json`、`.git/`（本地元数据）
- **记录人**：待补充

---

## 2026-11-25 22:32 ｜ 任务：建立协作文档与快捷指令集

- **任务**：创建修改日志、阶段清单、问题记录、快捷指令四份文档；打包为文件夹；编写 README；新增 GIT 同步指令。
- **用的工具**：Claude Code
- **提示要点**：规定 log 记录时间戳 / 概括 / 文件 / 代码 / 思路；stage 用无序清单并标注当前与下一阶段；problem 记录现存问题；fast 定义 UP / PUSH / PRB；后续补充 `GIT` 表示自动同步到指定仓库。
- **AI 给出的方案**：四份独立文档 + 读写路径约定；`UP` 更新 log/problem，`PUSH` 更新 stage，`PRB` 汇报问题；`GIT` 默认同步到 `main` 分支的 `ZHIXU/` 目录。
- **哪里错了 / 哪里不可靠**：初版指令集没有覆盖作业要求的 `AI_LOG.md`（当时尚未读 PDF）；在目录映射（P1）未解决时就把 `GIT` 写成可自动同步，实际执行可能失败或推错位置；`PUSH` 关键词容易与 git push 混淆，需在文档中反复注明。
- **最终怎么改**：文档中明确只有 `GIT` 会提交 / 推送、先 fetch、冲突即停、禁止强推；在 `problem.md` P1 标注 `GIT` 的依赖；读到作业 PDF 后新增 `AI_LOG.md` 并扩展指令。
- **涉及文件**：`指令集/log.md`、`指令集/stage.md`、`指令集/problem.md`、`指令集/fast.md`、`指令集/README.md`
- **记录人**：待补充

---

## 2026-11-25 22:40 ｜ 任务：阅读根目录资料并更新指令集

- **任务**：阅读 `Desktop\zhixu` 下的作业 PDF、命题库、工作流、架构图、配色文档与现有页面，按作业要求更新指令集。
- **用的工具**：Claude Code
- **提示要点**：阅读根目录下所有内容，更新指令集；此前确认过作业要求提交的 AI 记录（AI_LOG.md，六要素）。
- **AI 给出的方案**：逐页阅读 PDF 与架构图，提取 AI 使用政策、交付物、时间节点、页面现状；新增 `AI_LOG.md`，在 `fast.md` 增加 `AILOG` 并把 AI_LOG 纳入 `UP`；同步更新 stage / problem / README / log。
- **哪里错了 / 哪里不可靠**：先用 `pdftotext` 提取中文，结果大量乱码 / 丢字，不能作为依据；改用 PDF 逐页渲染阅读；根目录同时存在参考资料（color.md、color2.md）与业务代码，若不区分容易误判项目范围。
- **最终怎么改**：以逐页阅读结果为准，补充 AI_LOG 六要素与提交截止信息；按实际代码（搜索、分享、我的、编辑页的占位状态）修正 stage 与 problem；新增 `AI_LOG.md` 并补录本会话条目，标记为待组员核对。
- **涉及文件**：`指令集/AI_LOG.md`、`指令集/stage.md`、`指令集/problem.md`、`指令集/fast.md`、`指令集/README.md`、`指令集/log.md`
- **记录人**：待补充

---

## 2026-11-25 22:43 ｜ 任务：将 AI_LOG 统一放到 AI_details 目录

- **任务**：按用户要求，今后 AI 使用日志统一在项目根目录的 `AI_details/` 下更新，并同步指令集内的路径。
- **用的工具**：Claude Code
- **提示要点**：以后在 AI_details 里更新 AI_LOG。
- **AI 给出的方案**：确认 `AI_details/AI_LOG.md` 已存在；把 `fast.md`、`README.md`、`problem.md`、`stage.md` 中的维护目标与引用改为 `AI_details/AI_LOG.md`，并记录迁移。
- **哪里错了 / 哪里不可靠**：AI 一开始只关注移动文件本身，未先全局搜索引用；替换前仍有 4 处 `fast.md`、3 处 `README.md` 以及 problem / stage 中的旧路径，容易造成「文档说更新 A、实际读写 B」的不一致。
- **最终怎么改**：全局搜索并替换维护路径，保留历史日志里的旧路径不改写；验证新引用均指向 `AI_details/AI_LOG.md`，后续 `UP` / `AILOG` 都写入该文件。
- **涉及文件**：`AI_details/AI_LOG.md`、`指令集/fast.md`、`指令集/README.md`、`指令集/problem.md`、`指令集/stage.md`、`指令集/log.md`
- **记录人**：待补充

---
