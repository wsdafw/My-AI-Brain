# ADR-004: Governance Layer · 治理层与演进闭环

文档版本：1.0.0 | 架构目标：V1.1

更新时间：2026-11-11（Asia/Shanghai）

## Status

**Accepted（治理设计）**。决策人：PAIOS 负责人（用户）；记录日期：2026-11-11，依据本次明确建设要求。

验证状态：治理文档可以建设并检查；具体工作流程、量化阈值及首发验收范围仍为 Proposed。V1.1 没有正式发布，闭环效果尚待真实任务验证。

## Context

PAIOS 需要独立于 ChatGPT、Obsidian、DeepSeek 与 Codex 保存设计理念、架构、流程和历史决策。只增加工具或把规范留在平台项目指令中，难以维持长期一致性。

实际 Vault 已有目标目录及 17 个空白规范文件；用户随后明确允许填充这些空白文件，要求不覆盖已有内容的笔记。

## Decision

1. 采用 V1.1 的 L0–L5 六层结构，由 L0 定义和约束整个系统。
2. 将 `00_System/` 定为系统规范主来源；各工具使用带来源和版本的副本。
3. L5 经 Observe、Diagnose、Design、Implement、Evaluate、Standardize 将运行经验回流 L0。
4. 重要架构变更记录 ADR；正式流程需要实际验证和负责人接受，不能仅由 AI 起草即生效。
5. 以 Git 保存规范历史，采用 Major / Minor / Patch；每周复盘体验、每月复审架构，发布依赖证据而非日历。
6. 首次只跟踪治理文档的本地历史，保护现有业务笔记及配置；备份、远端与业务资产跟踪范围另行确定。

## Alternatives

| 方案 | 取舍 |
| --- | --- |
| 仅平台 Project Instructions | 使用方便，但设计历史与规范容易绑定平台 |
| 混入普通研究笔记 | 容易开始，但规范权威和生命周期不清晰 |
| 独立规范目录 + Git + 轻量 ADR | 符合当前本地环境，可追溯且保持简单；本次选择 |
| 复杂治理门户、数据库或自动化平台 | 目前没有必要性与收益证据 |

## Reasons

保持工具可替换，防止多份互相矛盾的规范，保存设计理由，并把实际改进证据连接到规范更新。

## Consequences

**Positive（预期）**：新工具或新会话可读取同一套规则；升级原因和验证过程可追溯。

**Negative**：需要人工复盘、维护链接与分发指令副本；过多记录会增加负担，因此只对重要变更建 ADR。

恢复/调整：保留 Git 历史及已接受决策；无效试行可停止，新的治理方式以新 ADR 替代，不删除原理由。

## Review Trigger

出现多份规范冲突、复盘不能形成改进、维护成本过高、工具替换仍丢失知识，或协作规模需要改变责任机制。

## Evidence and Links

[PAIOS](../PAIOS.md)、[ARCHITECTURE](../ARCHITECTURE.md)、[Evolution](../Workflows/Evolution.md)、[VERSIONING](../VERSIONING.md)、[建设记录](../GOVERNANCE-SETUP-2026-11-11.md)。
