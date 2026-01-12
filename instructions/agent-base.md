# Agent Base (Shared)

本文件作为所有自定义 Agent 的共享基座，用于统一：
- 文档结构与术语
- 指标口径与质量门禁（Gate）
- 通用模板与交付物定义
- 协作与交接（Handoff）标准

> 各角色文档应尽量“只写差异化内容”，通用规则引用本文件即可。

---

## 1. 通用术语

- **输入/输出契约（Contract）**：明确 Agent 在拿到哪些输入后，必须产出哪些输出；缺失输入时要先补齐哪些信息。
- **DoD（Definition of Done）**：交付完成的定义；用于评审/验收。
- **质量门禁（Quality Gate）**：不可越线的硬标准；未满足则不得进入下一阶段。
- **RACI**：R-Responsible 负责执行；A-Accountable 最终负责/拍板；C-Consulted 被咨询；I-Informed 被告知。

---

## 2. 文档统一骨架（建议）

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

---

## 3. 通用质量门禁（跨角色）

这些门禁建议默认启用，各角色可按需增删：

- **清晰度门禁**：关键术语有定义；关键决策有记录；Open Questions ≤ 10 条且有 Owner。
- **可追溯门禁**：需求/设计/实现/测试/发布可追溯（至少能从需求追到代码/测试/发布版本）。
- **风险门禁**：Top 5 风险清单齐全（概率×影响×应对）；高风险项必须有缓解方案。
- **安全门禁**：高危漏洞（Critical/High）= 0；秘密信息不入库（无硬编码 Token/Key）。
- **可观测门禁**：关键链路有指标/日志/告警；发布前演练过告警与回滚。

---

## 4. 通用交接协议（Handoff Contract）

每次交接至少包含：
- 背景（1 段话）
- 目标（可量化）
- 当前决策（Decision Log）
- 约束与假设（Constraints/Assumptions）
- 风险与待办（Risks/TODO）
- 交付物链接与版本号（Artifacts + Version）

---

## 5. 通用模板（摘录）

### 5.1 Decision Log（决策记录）
```
- Date:
- Decision:
- Options:
- Pros/Cons:
- Rationale:
- Impact:
- Owner:
```

### 5.2 Open Questions（待澄清问题）
```
- Question:
- Why it matters:
- Proposed answer:
- Owner:
- Due date:
```

### 5.3 Risk Register（风险登记）
```
- Risk:
- Likelihood (1-5):
- Impact (1-5):
- Score:
- Mitigation:
- Trigger:
- Owner:
```
