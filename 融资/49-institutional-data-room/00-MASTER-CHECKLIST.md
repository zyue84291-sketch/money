# 00 — Institutional Data Room Master Checklist

> 每项：`[ ]` 未准备 · `[x]` 已进 VDR · `Off-repo` 路径 + Owner · `doc_version` / As-of

## Legal

- [ ] Incorporation certificates, cap table **signed**, shareholder agreements  
- [ ] SAFE / SAFT / Token legal memo（若适用）  
- [ ] IP assignment / 开源许可 / 第三方依赖清单  
- [ ] 重大合同索引（客户、云、支付、数据）  
- [ ] 诉讼与争议声明  

## Finance

- [ ] Bank statements（摘要或 VDR 全本）  
- [ ] Treasury report（与 [`48`](../48-financial-engine/README.md) 同窗）  
- [ ] Management accounts + 与税务口径差异说明  
- [ ] Tax filings / 顾问信（按辖区）  

## Tech

- [ ] Audit reports（智能合约 + 渗透若有）  
- [ ] Uptime / SLO、事故报告（与 [`38`](../38-安全与审计体系-Security-Audit-System-骨架.md) 一致）  
- [ ] Architecture、依赖、infra 成本（月度）  
- [ ] 密钥与多签政策（**不含**密钥本体）  

## Product & Growth

- [ ] Analytics 定义 + 导出样例（与 [`02`](../02-经营真值-指标与财务-骨架.md) 同源）  
- [ ] Retention / cohort（[`46`](../46-pmf-validation/README.md)）  
- [ ] User growth 与 **获客渠道** 披露  

## Security

- [ ] Penetration test summary  
- [ ] Key management & rotation policy  
- [ ] Incident response runbook + 历史事件（若有）  

## 发前门禁

- [ ] **[`09`](../09-材料门禁与核对清单-骨架.md)** 全勾  
- [ ] **[`45`](../45-proof-of-execution/README.md)** 所有对外 URL 可点开  
- [ ] **[`59`](../59-ENTERPRISE-PRODUCTION-MATRIX.md)** 全表与 VDR **叶子节点** 对照无空项（本轮范围）

## 扩展索引（企业生产层）

- 商业化证据：[`53`](../53-commercial-gtm-pack/README.md)  
- 韧性 / 保险 / DPA / 隐私：[`54`](../54-enterprise-resilience-trust/README.md)  
- TS / 侧协议 / 银行金库：[`55`](../55-capital-legal-execution/README.md)  

---

**Owner**：CFO（Finance+Product 叶）+ CTO（Tech+Security 叶）+ 法务（Legal 叶）  
