# 01 — Runway Analysis（规格）

## Sheet：`Cash`

| 列 | 说明 |
|----|------|
| date |  |
| cash_begin |  |
| cash_in | 融资/收入 |
| cash_out | burn |
| cash_end |  |

## Sheet：`Runway`

- **Gross runway** = 现金 ÷ 最近 3 个月平均 burn  
- **Net runway** = 扣除 **已承诺支出**（租约、奖金、审计）后  
- **融资触发线**：现金 < ___ 个月 burn 时 **强制** 启动 bridge / 砍支（与 [`18`](../18-资本风控-Capital-Risk-Control-骨架.md) 一致）

## 输出

- 给 IC 的 **1 页图**：现金曲线 + 融资节点（非承诺日期，标为 scenario）。

---

**Owner**：CFO  
