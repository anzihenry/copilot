---
id: metrics-glossary
name: Metrics Glossary (Shared)
version: 0.2
last_updated: 2026-01-18
language: zh-CN
template: meta-info/meta_instruction.md
---
# Metrics Glossary (Shared)

本文件统一各类指标口径（建议值可按团队调整）。

---

## 目的（Purpose）
- 统一指标口径，便于跨角色对齐质量与效率目标

---

## 适用范围 / 不适用范围
**适用范围**：
- 所有角色文档中的指标与门禁引用

**不适用范围**：
- 具体项目的指标阈值制定（应在项目文档中定义）

---

## 优先级与冲突处理
- 项目若有更严格阈值，以项目阈值为准

---

## 约束（Constraints）
- 指标定义需可测量、可复现

---

## 规则（Rules）

### 1. 工程效能（DORA）
- **Deployment Frequency（部署频率）**：单位时间内生产发布次数。
- **Lead Time for Changes（变更前置时间）**：从代码合并到生产可用的时间。
- **Change Failure Rate（变更失败率）**：导致回滚/热修/事故的发布占比。
- **MTTR（平均恢复时间）**：事故从开始到恢复的平均时间。

建议门槛（可参考）：
- 变更失败率 ≤ 15%
- MTTR ≤ 60 分钟（按系统等级分层）

### 2. 性能指标
- **P50/P95/P99 延迟**：请求耗时分位数。
- **错误率**：5xx/4xx（或业务错误）占比。
- **吞吐量**：RPS/QPS。

建议门槛（示例）：
- 关键 API：P95 ≤ 200ms，错误率 ≤ 0.1%（按业务调整）

### 3. 质量指标
- **缺陷逃逸率（Escape Rate）**：上线后缺陷 / 总缺陷。
- **返工率**：因需求/设计/实现问题导致的返工工时占比。
- **测试覆盖率**：按仓库统计（行/分支/函数）。

### 4. 可用性与可靠性
- **SLA/SLO/SLI**：
  - SLI：指标（如可用性、延迟）
  - SLO：目标（如 99.9%）
  - SLA：对外承诺（通常不高于 SLO）

### 5. 前端体验（Web Vitals）
- **LCP**：最大内容绘制
- **CLS**：布局偏移
- **INP**：交互响应（替代 FID）

建议门槛（示例）：
- LCP ≤ 2.5s；CLS ≤ 0.1；INP ≤ 200ms

---

## 输入/输出契约（Contract）
**输入（Inputs）**：
- 团队/项目对指标的需求与定义

**输出（Outputs）**：
- 统一口径的指标定义

**缺失输入时的处理**：
- 默认采用行业通用定义，等待项目补充阈值

---

## 示例（Examples）
**Good**：
- 在角色文档中引用本文件的指标名与口径

**Bad**：
- 在不同角色文档里对同一指标给出不一致定义

---

## 参考（References）
- [instructions/agent-base.md](agent-base.md)

---

## Changelog
- 2026-01-18 v0.2 — 按 meta_instruction 模板重组结构
