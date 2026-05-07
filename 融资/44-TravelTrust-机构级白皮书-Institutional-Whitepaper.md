# TravelTrust — 机构级白皮书（Institutional Whitepaper）

**文档性质**：面向 **一级市场（VC / 战略投资 / 家办）** 与 **机构级 DD** 的 **叙事 + 架构 + 合规边界** 总览；**非**证券发行文件、**非**代币发售要约。  
**产品代号**：**TravelTrust**（与 `product-management-office/11-capital-narrative/02-解决方案与协议定位.md` 一致）。  
**真值与工程规格**：以主仓库 **`TT-Expedition-docs/spec/`** 为 SSOT；经营数字以 **`09-business-model/00-收入结构-佣金手续费增值服务.md` §0** 为唯一对外牵引入口；本白皮书 **不重复发明数字**。  
**版本**：`doc_version` **v0.9.1-enterprise** · **As-of**：2026-05-08  

---

## 重要声明（Legal Disclaimer）

1. **本文件不构成** 在任何司法辖区下的 **证券、集合投资计划或代币销售要约**；任何 Token 或股权条款 **以正式法律文件与已签 Term Sheet 为准**。  
2. **前瞻性陈述**（路线图、市场规模、财务预测）存在 **重大不确定**；实际结果可能与本文 **显著不同**。  
3. **监管状态** 为动态；本文所述 **法律定位** 为 **产品设计目标叙述**，**最终以法律意见书为准**（见 **`16-regulation-risk/05`** 登记与 `spec/08-4`）。  
4. 读者应 **自行聘请** 法律顾问与财务顾问；项目方 **不保证** 本文在读者所在地的 **合法性或可依赖性**。  

---

## 摘要（Executive Summary）

**TravelTrust** 针对跨境目的地服务中 **「先付后服」** 带来的 **信任、欺诈与支付摩擦**，用 **链上可验证托管（USDC Escrow）+ 链下规模化撮合与履约**，将 **「付款—履约—争议—结算」** 固化为 **可审计状态机**；在 **不承担银行存款机构责任** 的产品边界内，提升 **双边成交率、争议可执行性与资金终态透明度**。

**与 Web2 OTA / 私域全款 的差异**：OTA 擅长 **发现与抽佣**，但对 **私域成交与链上终态** 覆盖有限；私域全款 **缺少可托管、可仲裁执行** 的统一协议层。TravelTrust 将 **高价值争议与资金路径** 收敛到 **协议层**，将 **体验与运营** 留在 **链下**（混合架构见 **`spec/01`**）。

**一级市场阅读路径**：本文 **§2～§6** 对应 **Why now / Why us / Why win**；**§7～§9** 对应 **技术 + 安全 + 合规**；**§10～§12** 对应 **经济模型与增长**；**§13～§15** 对应 **终局、资金用途与风险**。**附录 A** 为 **PM Office 全量索引**，供 DD 按模块取证。

---

## 1. 行业背景与问题陈述

### 1.1 三条主线：Trust / Fraud / Payment

| 问题域 | 用户语言 | 协议与产品回应（工程锚点） |
|--------|----------|---------------------------|
| **Trust** | 陌生人目的地服务难信 | 向导准入、质押、评价、DID；**`spec/01` §4**、**`spec/64`** |
| **Fraud / Dispute** | 钱给了人跑了 / 扯皮难执行 | Escrow、争议窗口、仲裁与执行器；**`spec/01`**、**`spec/03`** |
| **Payment** | 跨境拒付、换汇、退款难 | Polygon USDC、链上终态与费用路由；**`spec/01` §5**、**`spec/14`** |

**Why now（机构常问的「时机」）**：稳定币结算渗透、体验经济与非标供给增长、远程工作与跨城复购、监管对 **可审计托管** 的期待上升——每条 **须** 在路演附录中挂 **数据来源与更新日期**（纪律见 **`11-capital-narrative/01-行业问题-Trust-Fraud-Payment.md`**）。

### 1.2 风险—收益对价（Risk vs Return）

机构评估 **「多承担一类风险，换回了什么商业对价」**。本项目将 **监管、供给质量、链上可用性** 等风险 **显式映射** 到 **扩张节奏、Take、准备金与技术预算**（执行表：**`09-business-model/04-规模化假设-十国到全球.md` §4**；口型：**`11/01` §4**）。**禁止** 无书面依据提高对外 **Take** 或 **补贴强度**。

---

## 2. 愿景与非目标

**愿景**：在合规边界内，成为全球目的地 **「信任与结算」** 的基础设施层之一——连接 **Traveler、Guide、生态伙伴** 的 **可验证交易闭环**。

**非目标（示例，与法务终稿一致）**：

- **非**持牌银行存款机构（除非已取得相应牌照并更新 **`16-regulation-risk/00`** §3）。  
- **非**无协议保障的 **「拉盘 / 保本」** 叙事；任何 Token 表述 **须** 符合 **`spec/82`、`spec/08-4`** 与 **`governance-token/LEGAL-SIGNOFF`**。  

---

## 3. 解决方案与协议定位

### 3.1 一句话定位

**TravelTrust 用链上托管（USDC Escrow）与可验证状态机，把「付款—履约—争议—结算」做成可审计闭环；撮合与社区在链下规模化。**

依据：**`spec/01`** 混合架构（〇节）。

### 3.2 混合架构原则

| 层 | 职责 | 说明 |
|----|------|------|
| **链上** | 资金托管路径、状态迁移、关键不变量、费用与释放 | 可审计、可回放；与 **`spec/10`**、**`spec/14`** 等一致 |
| **链下** | 发现、沟通、履约辅助、运营与增长 | 规模化与 UX；须符合 **`spec/13`**、**`14-ux-conversion`** |

### 3.3 与区域 / 治理扩展的关系

协议层 **区域、费用路由** 等叙事与 **`spec/83`、`spec/84`** 对齐；**融资材料** 须与 **`05-go-to-market/00-对外叙事与材料门禁`** 同序签核，避免 **地理叙事与工程参数漂移**。

---

## 4. 市场机会（TAM / SAM / SOM）

**方法论 SSOT**：**`11-capital-narrative/00-TAM-SAM-SOM-方法论与占位.md`**。

- **TAM**：全球可数字撮合的 **当地体验 / 向导类** 旅行服务年度支出池（**须第三方报告或授权引用**，禁止无来源「万亿」叙事）。  
- **SAM**：**合规可做 ∩ 支付可达 ∩ 产品形态匹配** 的子集；**SAM ≠ `spec/84` 地理列表的简单等同**（须法务剪枝）。  
- **SOM**：3 年内组织与资本可执行的 GMV / 收入 **上限三档**，与 **`09-business-model`** 现金流模型 **同一版本号** 发布。  

**牵引真值（Now）**：**`09-business-model/00` §0** — MAU、Escrow 活跃用户、30d GMV、Net Revenue、Take Rate、主漏斗转化率；**填实须 Data + Finance 双签**；对外前 **`11-capital-narrative/06-路演与DD数字对齐检查表.md`** 与 **`08-operations-pm/audit/01-跨模块一致性审计`** 无红。

**投资窗口（Investment Trigger）**：逻辑见 **`11-capital-narrative/README.md`** VC 六件套 §6（第二城复制证据、LTV/CAC、30d GMV 等 **与 `09/00` 同窗**）。**排除条件**：**现金 / 对账** 红灯时 **不得** 宣称窗口已开（**`09-business-model/06`** 等）。

---

## 5. 竞争格局与护城河（Why we win）

**结构化论证 SSOT**：**`13-positioning-competition/`**（竞品矩阵、替代方案、护城河类型拆解）。

**一句话论证（路演级）**：在「高客单、跨境、先付后服」场景下，对 **担心私域转账与纠纷的 Traveler** 与 **需要可信托管的 Guide**，相较 **当地私域全款** 与 **OTA 抽佣但不托管链上状态** 的替代方案，我们稳定交付 **「可审计 Escrow + 可解释争议窗口」**；证据链为 **`spec/01` / `spec/03` 状态机** + **试点城工单与链上对账样本（`99-real-world-validation/`）**（见 **`13-positioning-competition/00-Why-you-will-win-总纲.md`**）。

**护城河 = 可测指标（Moat Math）**：**不得** 使用无指标的「强网络效应」形容词。须能量化：**多 1 个活跃 Guide 对匹配/转化的 bp 改善**、**Escrow 路径下 dispute 率与重复进线率** vs 对照、**评分/凭证覆盖率对完成率的边际**（模板：**`10-growth-engine/00-从0到10万用户-总纲与里程碑.md` §5.1**；纪律：**`11-capital-narrative/02` §5**）。

**真实世界闭环（Reality Loop）**：`真用户 → 真 Escrow → 真 Net Revenue → 复购 → 再投资 → 组织扛压` — **SSOT**：**`11-capital-narrative/05` §5** + **`09/00` §0** + **`14-ux-conversion`** + **`12-org-scaling`**。

---

## 6. 用户与生态角色

| 角色 | 核心价值 | Office 参考 |
|------|----------|-------------|
| **Traveler** | 可预测的资金路径与争议救济 | **`14-ux-conversion`**、**`30-trust-safety`** |
| **Guide / 供给** | 履约后结算、信誉累积 | **`10-growth-engine`**、**`18-operations-strategy`** |
| **平台与伙伴** | 合规分润、生态飞轮 | **`25-ecosystem-partnerships`**、**`25/07` 网络效应飞轮** |

---

## 7. 协议架构与核心机制（摘要）

### 7.1 交易与状态

- **Escrow 生命周期**、**争议窗口**、**释放条件** 以 **`spec/01` §10**、**`spec/03`** 为准。  
- **费用（platformFeeBps）**、**计费与终态** 与 **`spec/01` §5**、**`spec/14`** 对齐；**Escrow 流水 ≠ 平台收入**（**`09-business-model/07`** 等口径）。  

### 7.2 支付与链

- **稳定币路径**（如 Polygon USDC）降低跨境摩擦；**RPC、索引、reorg、执行器** 风险 **须** 有 Runbook 与 **`19-risk-operations`** 运营响应。  

### 7.3 数据与 AI（基础设施叙事）

**数据仓库、事件流、风控与推荐** 的 **机构级描述** 见 **`39-data-ai-infrastructure`**（融资夹）与 PM Office **`32-ai-operating-layer`**、**`15-data-decision`**；**指标定义** 仍以 **`07-metrics-growth`** 与 **`spec/08-4`** 为 SSOT，**避免**「AI 驱动」口号与 **埋点真值** 脱节。

---

## 8. 安全、审计与运营韧性

**机构默认假设**：**无安全体系 = 无资格做资金相关协议。**

| 主题 | 索引 |
|------|------|
| **智能合约审计流程、Bounty、密钥、多签、事件响应** | 融资夹 **`38-安全与审计体系`**；工程 **`07-技术尽调`**、**`spec/15`** 附录〇发版门禁 |
| **审计报告与第三方背书索引** | **`20-机构信任层`**、**`14-机构级-Data-Room-Index`** Security 叶 |
| **资金异常、RPC 失败、黑天鹅升级** | **`19-risk-operations`**、**`36-anti-fragility-system`** |

---

## 9. 合规与法律定位

**公司一句话（Top Narrative）** — 与全 Office 对齐：

> **我们是**：一个基于 **Escrow** 的 **跨境旅游交易平台**，通过 **链上托管 + 链下履约**，在 **不承担金融托管责任** 的前提下，完成 **撮合、结算与争议处理**。（**`16-regulation-risk/00-跨境金融旅游-Web3-风险组合总览.md`**）

**风险域矩阵**（用户资金、个人数据、AML、证券与代币表述、消费者保护）与 **证据源、复盘频率** 见 **`16-regulation-risk/00` §1.1**；**「碰钱」法律边界** 须同读 **`16`** 相关 liability 与 **`spec/01`**。

**一级市场 DD 高频**：美国（证券、消费者披露、OFAC）；港新（VASP/支付/宣传边界）—— **矩阵填实** 见 **`16`** 各辖区文档。

---

## 10. Token、治理与价值捕获（若适用 · 强披露）

**本节仅为「若已纳入路线图」的披露框架**；若当前 **无 Token 发行** 或 **无公开销售**，须在对外材料中 **删除不适用环**，并与 **`26-endgame-strategy/00-路径谱系与披露门禁.md`** 一致。

| 主题 | SSOT |
|------|------|
| **Token 与股权叙事分轨** | **`26-endgame-strategy/02`**；**`spec/82`** |
| **行为 × 是否须 Token** | **`26-endgame-strategy/07-token-utility-binding`** |
| **Cap table 与解锁** | 融资夹 **`13-资本结构`**；工程 **`spec/81`** 等 |
| **二级市场运营边界（合规）** | **`21-Token-市场运营`** |

**禁止**：承诺价格、收益率或「必上所」时间表（除非已取得合规路径并完成 **`05-go-to-market`** 签核）。

---

## 11. 经济模型与单位经济

**收入结构**：交易抽成（take / platform fee）、未来可能的流量与增值服务 — **层级定义** 见 **`09-business-model/00` §1**；**与 `spec/83`「分配」层正交**（**`09/00` §2**）。

**单位经济（LTV / CAC、回本窗）**：**`09-business-model/02-单位经济模型-LTV-CAC.md`**。  
**现金流与商业闭环**：**`09-business-model/05-现金流与商业闭环-用户到再投资.md`**。  
**收入质量与确认**：**`29-finance-operating-system/05-Revenue-Quality-Layer`** 等。

---

## 12. 增长、规模化与执行路线

- **0→10 万用户机制与里程碑**：**`10-growth-engine/00`**。  
- **冷启动与城市模型**：**`10-growth-engine/01`**。  
- **双边市场策略**：**`10-growth-engine/02`**。  
- **第二城复制与 VC 问答证据**：**`23-scaling-playbook`**（如 **`23/04`**）。  
- **路线图优先级 P0/P1/P2**：**`17-execution-roadmap`**。  

**全球化与政治风险**：**`35-globalization-system`**（国家准入评分、政治风险层）。

---

## 13. 终局、退出与生态风险（非承诺）

**退出路径谱系**（IPO optionality、Token 流动性、并购）与 **披露红线**：**`26-endgame-strategy/00`**。  
**并购与战略买家情景**：**`26-endgame-strategy/03`**、**`06-acquirer-map`**。  
**集中度与依赖季更**：**`26-endgame-strategy/05-ecosystem-risk-dashboard`**。

---

## 14. 本轮资金用途（Use of Funds · 模板）

与 **`11-capital-narrative/README.md`** VC 六件套一致（比例可随轮次调整）：

| 桶 | 默认首稿比例 | 可验收里程碑（示例） |
|----|----------------|----------------------|
| **增长** | 40% | MAU / Escrow 用户 / 30d GMV（**`09/00` §0**）；CAC（**`10-growth-engine`**） |
| **供给** | 30% | 活跃 Guide、第二城复制（**`23/04`**） |
| **技术** | 20% | 对账绿、P0 资金为零（**`06-delivery-release`**、**`19-risk-operations`**） |
| **合规** | 10% | **`16`** 矩阵绿灯 + **`spec/08-4`** 可披露边界 |

**本轮金额与条款占位**：US$ ______；估值与轮次 — **`11-capital-narrative/05-资本路径-Seed到Series-A.md`**。

---

## 15. 组织、人才与治理

- **组织扩张与 RACI**：**`12-org-scaling`**。  
- **董事会与治理风险登记**：**`33-board-governance`**。  
- **CEO 经营操作系统与 Burn Multiple 一级市场口径**：**`27-ceo-operating-system`**（如 **`03-Burn-Multiple-Tracking`**）。  
- **人才与招聘 OS（融资夹扩展）**：**`40-talent-hiring-system`**。  

---

## 16. 风险因素（摘要）

非穷尽列举；完整登记见 **`16-regulation-risk`**、**`15-融资风险预案`**（融资夹）、**`36-anti-fragility-system`**。

1. **监管与合规** 变化导致 **市场收窄或产品改形**。  
2. **智能合约与链上基础设施** 漏洞、**第三方依赖**（RPC、索引、托管通道）。  
3. **双边冷启动** 与 **地推成本** 超预期。  
4. **竞争**（OTA、支付巨头、开源分叉）与 **Take 压缩**。  
5. **全球化执行** 与 **地缘政治** 对支付与运营的影响。  
6. **Token 若存在**：价格波动、流动性、证券法与营销边界。  
7. **关键人依赖** 与 **组织规模化** 失败（见 **`19-founder-narrative`**、**`40`**）。  

---

## 17. 参考一级市场白皮书的「结构对标」（非摘录）

同类 **已公开** 协议/基础设施白皮书，在机构侧常包含以下 **可扫描区块**（本项目已在 PM Office 与融资夹映射）：

| 常见区块 | TravelTrust 映射 |
|----------|------------------|
| Disclaimer / Regulatory | 本文首段 + **`16`** + **`spec/08-4`** |
| Abstract / Vision | §摘要 + §2 |
| Market & Problem | §1、§4 |
| Product & Architecture | §3、§7 |
| Tokenomics & Governance（若有） | §10 + **`13`、`26`、`43`** |
| Security & Audits | §8 |
| Roadmap | §12 + **`17`** |
| Team & Partners | §15 + **`25`** |
| Risk Factors | §16 |

**说明**：上表仅为 **结构对标**，不暗示与任何第三方 **文案或法律结构** 一致；**实质内容** 以 **`spec/`** 与 **已签署文件** 为准。

---

## 附录 A — `product-management-office` 全量导航（DD 取证用）

> **完整文件树与编号防呆** 以 **`../TT-Expedition-docs/product-management-office/README.md`** 与 **`00-架构总览与多维干系人地图.md`** 为准；下表为 **一级模块索引**。

| 模块 | 路径 | 典型 DD 问题 |
|------|------|----------------|
| 架构总览 | `00-架构总览与多维干系人地图.md` | 交付链 L1–L6 与支柱关系 |
| 战略 | `01-strategy/` | 愿景、非目标、边界 |
| 干系人 | `02-stakeholders/` | 权力/兴趣矩阵、合规接口 |
| 发现/定义 | `03-discovery/`、`04-definition/` | PRD、需求池 |
| GTM / Data Room 门禁 | `05-go-to-market/` | 对外顺序、索引 |
| 交付与发布 | `06-delivery-release/` | SLO、观测窗口 |
| 指标增长 | `07-metrics-growth/` | 指标字典、复盘节奏 |
| 运营 PM | `08-operations-pm/` | 一致性审计 |
| 商业模式 | `09-business-model/` | GMV、Take、现金流 |
| 增长引擎 | `10-growth-engine/` | 0→10 万、双边、裂变 |
| 融资叙事 | `11-capital-narrative/` | TAM、Why now、轮次、对齐表 |
| 组织扩张 | `12-org-scaling/` | 城市、RACI、KPI |
| 定位竞争 | `13-positioning-competition/` | Why you win |
| UX 转化 | `14-ux-conversion/` | 漏斗、Web2→Web3 |
| 数据决策 | `15-data-decision/` | 实验、阈值、A/B |
| 合规风险 | `16-regulation-risk/` | 辖区矩阵、碰钱边界 |
| 执行路线 | `17-execution-roadmap/` | P0–P2、里程碑 |
| 运营策略 | `18-operations-strategy/` | 本地 SOP、BD 节奏 |
| 运营风险 | `19-risk-operations/` | 资金异常、升级 |
| 产品迭代 | `20-product-iteration/` | Sprint、反馈 |
| 产品 OS | `21-product-operating-system/` | 原则、RICE、RACI |
| 经营驾驶舱 | `22-executive-dashboard/` | 北极星、Owner |
| 规模化手册 | `23-scaling-playbook/` | 第二城证明 |
| 品牌叙事 | `24-brand-narrative/` | Trust/Safety/Global |
| 生态伙伴 | `25-ecosystem-partnerships/` | 伙伴经济、飞轮 |
| 终局战略 | `26-endgame-strategy/` | IPO/Token/M&A 情景 |
| CEO OS | `27-ceo-operating-system/` | Burn、节奏 |
| 组织政治 | `28-org-politics-governance/` | 决策政治 |
| 财务 OS | `29-finance-operating-system/` | 收入质量 |
| Trust & Safety | `30-trust-safety-command-center/`、`30-trust-safety/` | 高风险旅客 Playbook |
| Board | `33-board-governance/` | 治理风险 |
| 技术战略 | `34-technology-strategy/` | 可用性战略 |
| 全球化 | `35-globalization-system/` | 国家评分、政治风险 |
| 反脆弱 | `36-anti-fragility-system/` | 崩溃演练 |
| AI 运营层 | `32-ai-operating-layer/` | Agent 责任矩阵、幻觉风险 |

**融资夹扩展（本地）**：**`10`～`22`、`37`～`43`、`44`（本文）** — 打法、投后、实体架构、安全体系、数据 AI、人才、危机、开发者、协议宏观治理等，见 **`README.md`**。

---

## 附录 B — 术语与缩写

| 术语 | 含义 |
|------|------|
| **Escrow** | 条件满足前约束释放的托管结算路径 |
| **GMV** | 成交总额；**Net Revenue** 为平台确认收入，二者不可混用 |
| **Take Rate** | Net Revenue ÷ 同窗 GMV |
| **SSOT** | Single Source of Truth，单一真值源 |
| **DD** | Due Diligence，尽职调查 |

---

## 企业级维护说明（与融资夹骨架同步）

- 各骨架文件（`01`～`09`、`10`～`22`、`37`～`43`）已增 **`## 企业级填充`** 段：为 **PM Office 可执行索引**，与本白皮书 **事实层同源**。  
- **数字与比例**：仍以 **`09-business-model/00` §0**、**`11/06`**、**`spec/08-4`** 为唯一真值；Office 或 `spec/` 变更后，须 **bump 本文 `doc_version`** 并复查 **附录 A** 行是否仍准确。  
- **新人 30 分钟入口**：`product-management-office/_registry/Day1-最小执行入口.md`；**主清单**：`PM-MASTER-CHECKLIST-从入职到发布-企业级.md`。

---

## 文档控制

| 字段 | 值 |
|------|-----|
| **Owner** | PM-O（须 CEO / CFO / 法务联席签署对外 PDF） |
| **对外 PDF 生成前** | 必过 **`09-材料门禁`**、**`11/06`**、**`08-operations-pm/audit/01`** |
| **修订** | 同步 bump **`doc_version`** 与 **As-of** |

---

**© 文档控制**：TravelTrust / TT-Expedition-docs 项目内部使用；对外分发须 **脱敏** 并附 **本文首段免责声明**。
