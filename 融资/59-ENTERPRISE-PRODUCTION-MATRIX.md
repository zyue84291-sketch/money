# 59 — Enterprise Production Matrix（企业级融资 — 主检表）

**用途**：一张表对齐 **「已有模板（本仓库）」** 与 **「仍需人类/原件（VDR/第三方）」**；开融资窗口前 **全表 review**。

## A. 叙事与证据（没有证据 = 不写进 IC）

| # | 交付物 | 模板位置 | 原件 / 真值位置 | Owner |
|---|--------|----------|-----------------|-------|
| 1 | 可点开产品证明 | [`45-proof-of-execution`](./45-proof-of-execution/) | URL 实测 + VDR | 工程 |
| 2 | 用户与留存 | [`45/01`](./45-proof-of-execution/01-real-user-proof.md)、[`46`](./46-pmf-validation/) | BI 导出 | 数据 |
| 3 | PMF 需求图 | [`46/00`](./46-pmf-validation/00-user-demand-map.md) | 访谈纪要 | 产品 |
| 4 | 壁垒与竞品拆解 | [`47`](./47-moat-system/) | 第三方数据 | 战略 |
| 5 | 时代叙事 | [`50`](./50-meta-narrative/) | 不与事实矛盾 | CEO |

## B. 财务与资本（没有模型版本 = 不谈估值）

| # | 交付物 | 模板位置 | 原件 / 真值位置 | Owner |
|---|--------|----------|-----------------|-------|
| 6 | Burn / Runway / 情景 | [`48-financial-engine`](./48-financial-engine/) | `.xlsx` 仅 VDR | CFO |
| 7 | 经营双签数字 | [`02`](./02-经营真值-指标与财务-骨架.md) | 财务系统 | CFO |
| 8 | TS 就绪与侧协议 | [`55`](./55-capital-legal-execution/) | 律所工作区 | 法务 |
| 9 | Cap table | [`13`](./13-资本结构-Cap-Table-Tokenomics-骨架.md) | 律所签字表 | CFO |

## C. 信任、合规、韧性

| # | 交付物 | 模板位置 | 原件位置 | Owner |
|---|--------|----------|----------|-------|
| 10 | Data Room 主清单 | [`49`](./49-institutional-data-room/)、[`14`](./14-机构级-Data-Room-Index-骨架.md) | VDR | CFO/CTO/法务 |
| 11 | BCP/DR、保险 | [`54`](./54-enterprise-resilience-trust/) | 保单、演练记录 | CTO/CFO |
| 12 | 子处理者与隐私 | [`54/02`](./54-enterprise-resilience-trust/02-subprocessors-dpa-index.md)、[`54/03`](./54-enterprise-resilience-trust/03-privacy-dd-summary.md) | DPA | 法务 |
| 13 | 审计与密钥政策 | [`38`](./38-安全与审计体系-Security-Audit-System-骨架.md)、[`20`](./20-机构信任层-Institutional-Trust-Layer-骨架.md) | 审计 PDF | CTO |

## D. 商业与增长

| # | 交付物 | 模板位置 | 原件位置 | Owner |
|---|--------|----------|----------|-------|
| 14 | 标杆客户与案例 | [`53`](./53-commercial-gtm-pack/) | 合同/同意书 | 销售 |
| 15 | 分渠道单位经济 | [`53/04`](./53-commercial-gtm-pack/04-channel-unit-economics.md) | 模型与 BI | 增长/CFO |

## E. 流程与 IC

| # | 交付物 | 模板位置 | 说明 | Owner |
|---|--------|----------|------|-------|
| 16 | CRM / 跟进 / FAQ | [`52`](./52-investor-ops/) |  | CEO/COO |
| 17 | IC 一页与 DD 日志 | [`57`](./57-diligence-ic-pack/) |  | CEO |
| 18 | 对外版本登记 | [`57/02`](./57-diligence-ic-pack/02-document-version-register.md) |  | COO |
| 19 | 材料门禁 | [`09`](./09-材料门禁与核对清单-骨架.md) | **发包前强制** | CEO |

## F. 仍无法被模板替代（须 consciously 生产）

- **独立第三方**：审计聘用信、律所 scope、财务 DD 配合承诺。  
- **链上–链下对账调节表**（样本 Tx + 订单 ID）。  
- **监管对话书面边界**（oral 不得对外写成背书）。  
- **英文材料等价**（[`58/02`](./58-glossary-media-pack/02-bilingual-parity-checklist.md)）。  
- **董事会/股东会纪要**中与融资相关的决议索引。  
- **期权与招聘时间线**与 runway 对齐（[`40`](./40-人才与组织-Talent-Hiring-OS-骨架.md)、[`48`](./48-financial-engine/README.md)）。  

---

**更新频率**：每周五 **15 min** 站会过本表；**Partner 会议前** 全勾。

**Owner**：CEO  
