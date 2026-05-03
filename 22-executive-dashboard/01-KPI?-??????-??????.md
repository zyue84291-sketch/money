# 01 — KPI 树（公司 → 产品 → 功能）

**用途**：把 **`22/00`** 北极星 **分解** 为可 owner、可周报的枝；**阈值与实验** 细节在 **`15`**。

---

## 1. 三层结构（模板）

```text
公司级（Board / CEO）
├── 北极星（22/00）
├── 增长：供给 / 需求 / 漏斗
├── 收入：Take rate × 可计费 GMV、增值服务
└── 风控：欺诈率、争议率、资金异常 SLA、合规 incident
```

```text
产品级（CPO / Head of Product）
├── 核心路径：Visit → 下单 → Escrow → 完结 → 评价
├── 双边：活跃 Guide、活跃 Traveler、匹配效率
└── 平台：RPC 成功率、索引延迟（与工程共 owner）
```

```text
功能级（Squad / Epic）
├── 具体 Feature 的 adoption、错误率、客服工单占比
└── 每个 Epic 必须挂 ≥1 个 **公司树叶子** 指标
```

---

## 2. 与现有 Office 目录的映射

| KPI 枝 | 主文档 |
|--------|--------|
| 增长机制 | **`10-growth-engine/`**、**`18-operations-strategy/`** |
| 漏斗与转化 | **`14-ux-conversion/`** |
| 实验与阈值 | **`15-data-decision/`** |
| 埋点与口径 | **`07-metrics-growth/`** |
| 风险与异常 | **`19-risk-operations/`**、**`16-regulation-risk/`** |

---

## 3. 变更记录

| 日期 | 变更 |
|------|------|
| 2026-05-02 | 初版 |
