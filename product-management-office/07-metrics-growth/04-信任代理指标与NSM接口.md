# 04 — 信任代理指标（Trust KPI）与 NSM 接口

**用途**：把 **`14/02`** 理念文档 **可量化**，使「信任设计 → 转化」**可实验、可证伪**。

---

## 1. 北极星（NSM）

**当前默认（管理层可改，须书面）**：**每周 Escrowed GMV**（`weekly_escrowed_gmv`）。  
**备选**：每周 **Completed** 订单数 —— 与 **`09-business-model`** GMV 定义对齐后再切换。

**绑定**：**`22/04`** 叶子 + **`15/00` §1**。

---

## 2. `trust_score_proxy`（叶子指标 · 可二选一跑实验）

| 版本 | **定义（公式）** | **分子事件（占位）** | **分母事件（占位）** | **来源** | **决策用途** |
|------|------------------|----------------------|----------------------|----------|----------------|
| **A（默认）** | `escrowed_sessions / payment_page_sessions` | `order_escrowed`（链上确认后投影） | `checkout_payment_view` | **DB + on-chain** | **↑ 表信任 + 支付摩擦下降** |
| **B（信任文案）** | `commits_after_trust_doc / trust_doc_expand` | `commit_order` | `trust_fund_flow_expand` | **DB** | **↑ 用户愿点「资金说明」后仍转化** |

**归属漏斗**：A → **`funnel_commit_to_escrow`**；B → **`funnel_intent_to_commit`**。

**阈值（示例）**：若 **A < 0.55** 连续 **2 周** → 冻结「简化文案」类实验，**优先** 钱包/链上稳定性（联动 **`07/02`** Commit→Escrow 红线）。

---

## 3. 最小证明链：**trust → escrow_conversion → GMV**（**否则信任工作不上 CFO 表**）

```text
trust_score_proxy_a  ↑（同一 7 日窗）
        ⇒ 预期 escrow_conversion_rate  ↑
                ⇒ 预期 weekly_escrowed_gmv  ↑
```

| 次序 | 指标 | **同窗** | **判读** |
|------|------|----------|----------|
| 1 | **`trust_score_proxy_a`** | 7 日 | 信任/支付页摩擦 **代理** |
| 2 | **`escrow_conversion_rate`**（L1） | 7 日 | **必须**与 trust **同向**或解释根因（RPC、合约） |
| 3 | **`weekly_escrowed_gmv`**（NSM） | **自然周** | **周会唯一主结论** |

**否决规则**：**trust ↑ 且 escrow flat/down** → **信任叙事不得全量**；**转** **`EXP-0142`** 类钱包/链上实验（**`00` §2** 因果句）。

---

## 4. Data → Decision（摘要）

**每日 / 周** 写死流见 **`../15-data-decision/04-数据驱动迭代与会议节奏.md` §2.1 / §2.2**。

## 变更记录

| 版本 | 日期 | 说明 |
|------|------|------|
| 0.1.0 | 2026-05-02 | 初版：Trust proxy + NSM 接口 |
| 0.2.0 | 2026-05-02 | **§3** trust→escrow→GMV 证明链 + **§4** 链 `15/04` |
| 0.3.0 | 2026-05-05 | 文末 **Owner / 更新日期 / 下次评审** |

---

**Owner**：信任研究 / 数据 PM（代理指标）+ 增长（NSM 同窗）  
**更新日期**：2026-05-05  
**下次评审**：**月**（与 **`07/00`**、`07/08` 异常解读 **同周**）

