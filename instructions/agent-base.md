---
id: agent-base
name: Agent Base (Shared)
version: 0.3
last_updated: 2026-01-18
language: zh-CN
template: meta-info/meta_instruction.md
---
# Agent Base (Shared)

本文件作为所有自定义 Agent 的共享基座，用于统一：
- 文档结构与术语
- 指标口径与质量门禁（Gate）
- 通用模板与交付物定义
- 协作与交接（Handoff）标准

> 各角色文档应尽量“只写差异化内容”，通用规则引用本文件即可。

---

## 目的（Purpose）
- 统一 Agent 文档的结构、术语与质量门禁
- 提供跨角色通用模板与交接协议

---

## 适用范围 / 不适用范围
**适用范围**：
- 本仓库所有 Agent 角色文档

**不适用范围**：
- 业务/产品需求本体的制定
- 项目执行细节（应归属各角色文档）

---

## 优先级与冲突处理
- 角色文档若与本基座冲突，以角色文档的“差异化约束”优先
- 安全与合规相关门禁优先级高于其他建议项

---

## 约束（Constraints）
- 保持术语口径一致；新增术语需在本文件补充定义
- 关键门禁不得被移除，除非明确说明替代方案

---

## 规则（Rules）

### 通用术语
- **输入/输出契约（Contract）**：明确 Agent 在拿到哪些输入后，必须产出哪些输出；缺失输入时要先补齐哪些信息。
- **DoD（Definition of Done）**：交付完成的定义；用于评审/验收。
- **质量门禁（Quality Gate）**：不可越线的硬标准；未满足则不得进入下一阶段。
- **RACI**：R-Responsible 负责执行；A-Accountable 最终负责/拍板；C-Consulted 被咨询；I-Informed 被告知。

### 文档统一骨架（建议）
每个角色文档建议遵循如下结构：

1) YAML Front Matter（id/name/version/last_updated/owner/scope）
2) 角色描述
3) 适用范围 / 不适用范围
4) 输入/输出契约（Contract）
5) 核心职责与标准化流程（每条职责都要含：流程、指标、交付标准）
6) 工具与技能栈（按类别）
7) 质量门禁（Gate）
8) 模板（Checklist/Doc Skeleton）
9) KPI（用于复盘与绩效）
10) 协作与交接（Handoff + RACI）
11) Changelog

### 通用质量门禁（跨角色）
这些门禁建议默认启用，各角色可按需增删：

- **清晰度门禁**：关键术语有定义；关键决策有记录；Open Questions ≤ 10 条且有 Owner。
- **可追溯门禁**：需求/设计/实现/测试/发布可追溯（至少能从需求追到代码/测试/发布版本）。
- **风险门禁**：Top 5 风险清单齐全（概率×影响×应对）；高风险项必须有缓解方案。
- **安全门禁**：高危漏洞（Critical/High）= 0；秘密信息不入库（无硬编码 Token/Key）。
- **可观测门禁**：关键链路有指标/日志/告警；发布前演练过告警与回滚。

### 通用交接协议（Handoff Contract）
每次交接至少包含：
- 背景（1 段话）
- 目标（可量化）
- 当前决策（Decision Log）
- 约束与假设（Constraints/Assumptions）
- 风险与待办（Risks/TODO）
- 交付物链接与版本号（Artifacts + Version）

### 通用模板（摘录）

#### Decision Log（决策记录）
```
- Date:
- Decision:
- Options:
- Pros/Cons:
- Rationale:
- Impact:
- Owner:
```

#### Open Questions（待澄清问题）
```
- Question:
- Why it matters:
- Proposed answer:
- Owner:
- Due date:
```

#### Risk Register（风险登记）
```
- Risk:
- Likelihood (1-5):
- Impact (1-5):
- Score:
- Mitigation:
- Trigger:
- Owner:
```

---

## 输入/输出契约（Contract）
**输入（Inputs）**：
- 角色文档草稿
- 角色的核心职责、流程与门禁定义

**输出（Outputs）**：
- 统一结构的角色文档
- 标准化术语与门禁引用

**缺失输入时的处理**：
- 先补齐角色职责与交付标准，再完善其余内容

---

## 示例（Examples）
**Good**：
- 角色文档仅补充差异化内容，其余引用本基座

**Bad**：
- 角色文档重复粘贴通用门禁与模板

---

## 参考（References）
- [instructions/metrics-glossary.md](metrics-glossary.md)

---

## Changelog
- 2026-01-18 v0.3 — 按 meta_instruction 模板重组结构
