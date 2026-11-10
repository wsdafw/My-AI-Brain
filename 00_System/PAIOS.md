# PAIOS · 系统总纲

文档版本：1.0.0 | 架构目标：V1.1 | 状态：Accepted（治理基线）

更新时间：2026-11-11（Asia/Shanghai） | 系统负责人：Vault 所有者

## 我们在建设什么

Personal AI Operating System（PAIOS）是一套长期支持个人研究、学习、开发和创造的工作系统。系统由目标、原则、架构、知识资产、执行流程、验证证据和历史决策组成。

**PAIOS 是系统本身；ChatGPT、DeepSeek、Obsidian、Python、Git、VS Code 与 Codex 都是可替换的工具。** 更换工具时，应保留目标、规范、可读的知识资产、工作流程和决策历史。

## 当前基线与事实边界

- 本次接受 L0–L5 架构方向、本地 Markdown 规范库和证据驱动的演进原则。
- 目标系统版本为 `1.1.0`，发布状态为 **Proposed / 未发布**。文档版本 `1.0.0` 只表示本文首版，不代表系统已通过验证。
- 本次检查没有发现可核实的 V1.0 正式发布记录；不补造旧版本或旧实验结果。
- `Accepted` 表示负责人已选择该方向，**不等于效果已验证**。尚未运行的流程、接口和指标阈值保持 `Proposed`。
- 初始目录、已有笔记、未确认事项及交付清单见[建设记录](GOVERNANCE-SETUP-2026-11-11.md)。

## 系统规范唯一来源

`00_System/` 是 PAIOS 系统规范的唯一可信来源（Source of Truth），并用 Git 保留历史。聊天、平台项目指令和工具配置只承载应用副本；不能自行成为第二套系统规范。研究事实仍需证据支持，存入此目录不意味着事实自动成立。

采用顺序：先读本文与原则，再读架构、相关 Accepted ADR，最后读取任务流程及 AI 指令。Proposed 内容必须显式标明试行。发现同一范围内的规范冲突时，记录冲突并交由负责人裁定，不按文件新旧或模型偏好悄悄覆盖。

## 规范导航

| 文件 | 回答的问题 |
| --- | --- |
| [VISION](VISION.md) | 长期目标与成功状态 |
| [PRINCIPLES](PRINCIPLES.md) | 系统必须遵循什么原则 |
| [ARCHITECTURE](ARCHITECTURE.md) | L0–L5 如何协作、工具如何替换 |
| [ROADMAP](ROADMAP.md) | 下一步做什么、何时可以推进 |
| [CHANGELOG](CHANGELOG.md) | 发生了哪些已记录的变化 |
| [EVALUATION](EVALUATION.md) | 如何测量升级效果 |
| [VERSIONING](VERSIONING.md) | 版本、状态、Git 与发布规则 |
| [Research](Workflows/Research.md) / [Learning](Workflows/Learning.md) / [Development](Workflows/Development.md) | 三类任务的标准流程草案 |
| [Review](Workflows/Review.md) / [Evolution](Workflows/Evolution.md) | 周月复盘与六步演进闭环 |
| [Global](AI_Instructions/Global.md) | 通用 AI 行为规则与交接格式 |
| [研究指令](AI_Instructions/Research.md) / [学习指令](AI_Instructions/Learning.md) / [开发指令](AI_Instructions/Development.md) | 角色专用规则 |
| [ADR-001](Decisions/ADR-001.md) / [ADR-002](Decisions/ADR-002.md) / [ADR-003](Decisions/ADR-003-Model-Agnostic-Harness.md) / [ADR-004](Decisions/ADR-004-Governance-Layer.md) | 知识库、AI 工作空间、Harness 与治理架构的选择依据 |
| [EXP-001](Experiments/EXP-001-Research-Capture.md) | 首个待执行的系统改进实验 |

## 最小使用方式

1. 明确本次任务的问题、交付物和验收条件，选择对应工作流程。
2. 给所用 AI 提供当前规范版本及相关文件；无法读取时说明缺失，不假装已加载。
3. 将结果以 Markdown 保存到实际存在的业务目录，注明来源、假设和未完成项。
4. 在复盘中发现问题，按 Evolution 流程试验；有效且经负责人接受后才更新正式规范。

## 治理责任与边界

负责人决定架构取舍、接受或拒绝重要决策以及正式发布。AI 可以在已授权范围内起草、实现和验证；不能把自己的建议默认为已接受决策。

本次只建设轻量规范层，不安装插件、不新增复杂自动化、不迁移业务笔记。未来重要架构变更必须记录 ADR；日常笔记与文字纠错不要求额外建立 ADR。
