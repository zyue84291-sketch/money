# 03 — Treasury Risk Model（规格）

## Sheet：`Balances`

| asset | chain | address_ref | amount | haircut_% | USD_equiv |
|-------|-------|---------------|--------|-----------|-----------|

- `address_ref`：指向 VDR 或内部 vault 登记，**不**在 Git 写完整私钥相关。

## Sheet：`Concentration`

- 单一稳定币 / 单一托管方 / 单一链 **占比** 阈值与 **迁移预案**。

## Sheet：`Stress`

- 脱锚、交易所暂停、RPC 级联失败时的 **72h 动作**（与 [`38`](../38-安全与审计体系-Security-Audit-System-骨架.md) 一致）。

---

**Owner**：CFO + 金库多签 Owner  
