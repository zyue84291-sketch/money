# 00 — Burn Rate Model（规格）

## Sheet：`Actuals_Monthly`

| 列名 | 类型 | 说明 |
|------|------|------|
| month | date YYYY-MM | 关账月 |
| opex_payroll | currency | 含雇主成本 |
| opex_infra | currency | 云、RPC、数据 |
| opex_marketing | currency | 可拆 paid / organic |
| opex_legal_compliance | currency |  |
| opex_other | currency |  |
| **total_burn_cash** | formula | 上列求和（与银行流出对拍） |
| notes | text | 一次性费用标注 |

## Sheet：`Forecast`

- 未来 **24–36 个月** 假设：**HC 计划**、**市场实验上限**、**合规里程碑费用**。  
- 每个假设格旁 **Owner + 最后同意日期**。

## 与 `02` 对拍

- `total_burn_cash` 必须与 **管理报表 / 银行** 同窗；差异进 **调节表**。

---

**Owner**：CFO  
