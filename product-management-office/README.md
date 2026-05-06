# TravelTrust · 企业级产品管理办公室（PM Office）

**一句话**：**TravelTrust PM Office** = 公司级 **产品操作系统** —— **决策 + 执行 + 验证**，并与 **`spec/`**（工程 SSOT）、**`go-live`**（发布门禁）、**`99`**（真实世界验证）联动；**不是**文档库、**不是** Wiki 合集、**不是** PPT。

**受众**：产品负责人 / 高级 PM —— 模块边界、干系人地图、上线前后检查点、企业级 **可追溯** 责任链。

**新人第一天 / 最小执行入口**（≤30 min）：**[`_registry/Day1-最小执行入口.md`](_registry/Day1-最小执行入口.md)**  
**团队听得懂的一页版**（宣贯、周会开场）：**[`_registry/讲得清-团队表达层.md`](_registry/讲得清-团队表达层.md)**  
**每一条新需求 / 进需求评审前**（强制）：**[`_registry/新需求-最小入口-模板.md`](_registry/新需求-最小入口-模板.md)** —— **缺块 = 当场拒收、不讨论方案**（**`08/meetings/01` §1.2**）

**产品边界只有三件事**（其余都可以做；详见 **`01-与工程-spec-SSOT-对齐契约.md`** 文首与 **`00` §1.11**）：

1. **不定义技术真值** —— 那是 **`spec/`**。  
2. **不绕过资金语义** —— 以 **`spec/`** 与链上为准。  
3. **不单模块拍板** —— 必须 **`02` Impact Map** + **`21`**。  

**新产品经理 · 从入职到发布 — 企业级完善主清单（可逐项勾选）**：**[`PM-MASTER-CHECKLIST-从入职到发布-企业级.md`](PM-MASTER-CHECKLIST-从入职到发布-企业级.md)**  
**15 天、每天 5 小时、全 Office 交付**：**[`PM-15天冲刺-每日5小时-全文件完成清单.md`](PM-15天冲刺-每日5小时-全文件完成清单.md)**（附录 §B 路径勾选 **以该文文首 rg 数为准**；含 **`27`～`36` 扩展支柱**；与主清单关系见该文）  
**新同学上手**：**[`_registry/Day1-最小执行入口.md`](_registry/Day1-最小执行入口.md)** → **[`_registry/新成员上手路径-Day1-Day7-Day30.md`](_registry/新成员上手路径-Day1-Day7-Day30.md)** · **团队版** **[`_registry/讲得清-团队表达层.md`](_registry/讲得清-团队表达层.md)** · **违规后果与当场执行**：**[`01-与工程-spec-SSOT-对齐契约.md`](01-与工程-spec-SSOT-对齐契约.md)** §2.5～§2.5.1 · **记 log**：**[`_registry/违规记录.md`](_registry/违规记录.md)** · **会议绑定**：**[`08-operations-pm/meetings/01-Meeting-OS-规则与会议绑定.md`](08-operations-pm/meetings/01-Meeting-OS-规则与会议绑定.md)** · **每日执行**：**[`_registry/执行检查清单-每日版.md`](_registry/执行检查清单-每日版.md)** · **Office 周检（系统本身）**：**[`_registry/Office运行健康度-System-Health-周检.md`](_registry/Office运行健康度-System-Health-周检.md)** · **月决策复盘**：**[`21-product-operating-system/07-决策复盘机制-Decision-Review.md`](21-product-operating-system/07-决策复盘机制-Decision-Review.md)** · **规则→人**：**[`_registry/规则绑定与执行责任.md`](_registry/规则绑定与执行责任.md)** · **反官僚**：**[`_registry/反官僚原则.md`](_registry/反官僚原则.md)**

## 与仓库其他目录的关系

| 目录 | 职责 |
|------|------|
| **`spec/`** | 技术、协议、API、合约、合规 **单一事实来源（SSOT）**；产品决策不得与之冲突。 |
| **`product-manager/`** | 既有 **决策包、融资、增长、任务母表** 等执行资料；本 Office **不替代**其正文，可互链。 |
| **`product-management-office/`（本目录）** | 本 Office：跨模块 **PRD/决策/评审/上线/复盘** 的规则、模板与 Impact 契约；**`_registry/`** 提供 **新人第一天、团队表达层、需求票、违规记录、Office 周检** 等强执行入口；**`08/…`** 将 **`cadence`（周/月/季）** 与 **`meetings`（会议绑定）** 落到议程（例如 **`22`→`15`→`21`** 链路）；主线支柱 **`09`～`26`**；扩展支柱 **`27`～`36`**（CEO OS、组织政治、财务 OS、T&S、真值治理、AI、董事会、技术战略、全球化、反脆弱）；与 **`spec/`** 撞号时（例如 **`spec/15`** vs **`15-data-decision`**、**`spec/34`** vs **`34-technology-strategy`**）须写 **全路径**，禁止口头简称混用。 |

## 文档树（目录结构）

```text
product-management-office/
├── README.md
├── PM-MASTER-CHECKLIST-从入职到发布-企业级.md   ← 新产品经理按优先级完善 Office 的主清单
├── PM-15天冲刺-每日5小时-全文件完成清单.md     ← 15×5h 全文件完成（冲刺档）
├── 00-架构总览与多维干系人地图.md
├── 01-与工程-spec-SSOT-对齐契约.md
├── 02-系统联动规则与模块Impact-Map.md    ← 跨模块输入/输出/Impact（非新子目录）
├── _registry/
│   ├── Day1-最小执行入口.md                 ← 新人第一天 ≤30min
│   ├── 讲得清-团队表达层.md                 ← 全员：名词→人话
│   ├── 新需求-最小入口-模板.md               ← 每条 REQ 强制复制进 PRD
│   ├── Day1-Owner-范围登记.md               ← 冲刺 / 季初：Owner 与 PM↔spec 边界（模板）
│   ├── 权限边界-强执行.md                   ← 谁可改 spec / PRD / 商业 / 上线
│   ├── 新成员上手路径-Day1-Day7-Day30.md   ← Onboarding 日历路径
│   ├── 违规记录.md                          ← 违规当场处置 + 时间线 log（反滥用）
│   ├── 执行检查清单-每日版.md               ← 防「纸上系统」
│   ├── 规则绑定与执行责任.md               ← 规则 → 具体人
│   ├── 反官僚原则.md                        ← 文档/会议/数据 vs 结果
│   ├── Office运行健康度-System-Health-周检.md  ← 规则是否在跑（周）
│   └── …
├── 01-strategy/ … 08-operations-pm/          ← 交付主线（**`08/…/cadence/`** = 周/月/季节奏）
├── 09-business-model/
├── 10-growth-engine/
├── 11-capital-narrative/
├── 12-org-scaling/
├── 13-positioning-competition/             ← Why you will win（结构化竞品与护城河）
├── 14-ux-conversion/                         ← 漏斗、Onboarding、信任、Web2↔Web3
├── 15-data-decision/                         ← 阈值、A/B、**实验系统 05～06**（≠ spec/15）
├── 16-regulation-risk/                       ← DD 友好：KYC/AML/多国矩阵/预案索引
├── 17-execution-roadmap/                     ← 产品级执行：路线、里程碑、P0/P1/P2、资源（≠ spec/17 MVP清单）
├── 18-operations-strategy/                   ← GTM 实战：城市0→100单、招募、SOP（05深化 + 10落地）
├── 19-risk-operations/                       ← 运营级异常/争议/投诉 SOP（≠ spec/19 Escrow参数）
├── 20-product-iteration/                     ← 反馈、Sprint、优先级、PM 决策（≠ spec/20 云架构）
├── 21-product-operating-system/              ← 跨模块决策、冲突规则、原则、PM 边界、决策复盘（≠ spec/21 UI3D）
├── 22-executive-dashboard/                   ← **NS+`04`全模块KPI绑定**、**`06` 周会30min执行纸**、KPI 树、监控、复盘（≠ spec/22 Design Tokens）
├── 23-scaling-playbook/                      ← 试点→封包→复制；城市/组织 handover（≠ spec/23 Figma）
├── 24-brand-narrative/                       ← 用户心智、信任叙事、PR/KOL/Web3 传播（≠ spec/24 文档整理结论）
├── 25-ecosystem-partnerships/               ← OTA/供给/Web3/支付合规伙伴地图（≠ spec/25 顶级UI标准）
├── 26-endgame-strategy/                      ← IPO/Token/并购/网络效应终局（≠ spec/26 文档审计报告）
├── 27-ceo-operating-system/                  ← CEO OS：周生死判断、叙事漂移、创始人日志、Burn multiple…
├── 28-org-politics-governance/               ← 组织政治：权力冲突、激励错位、Bus factor、影子决策
├── 29-finance-operating-system/              ← CFO 层：Burn、库务、Escrow 资金图、Runway、情景、收入质量
├── 30-trust-safety-command-center/         ← T&S 指挥：高风险旅客、封禁、欺诈情报、Geo、War Room
├── 31-truth-governance/                      ← 数据防伪：指标作弊、假 GMV、Override、Board 口径认证
├── 32-ai-operating-layer/                    ← AI 治理：Agent RACI、升级、幻觉、人机闭环、AIGC、实验
├── 33-board-governance/                      ← 董事会：决议、投资人权利、down-round、危机披露、RPT
├── 34-technology-strategy/                   ← CTO 战略（≠ spec/34 数据类型对齐表）
├── 35-globalization-system/                  ← 全球化：国家评分、FX、本地化、税务矩阵、政治风险
├── 36-anti-fragility-system/                 ← 反脆弱：崩溃演练、死亡螺旋、挤兑、舆情、创始人退出、监管关停
├── 99-real-world-validation/                 ← 真人/试点/GMV&漏斗验证与证据闭环（≠ spec/27-P* 实现记录）
└── appendices/
```

## 建议阅读顺序

### A. 产品负责人（全栈）

1. **`00-架构总览与多维干系人地图.md`**（**`09`～`26` 支柱全景**，然后 **`02` 联动**、**`99` 验证**）  
2. **`01-与工程-spec-SSOT-对齐契约.md`**  
3. **`02-系统联动规则与模块Impact-Map.md`**（**改 14 会不会震 19/09** — 强连接规则）  
4. **`99-real-world-validation/README.md`**（**真人、试点、GMV/漏斗证据**）  
5. **`21-product-operating-system/README.md`**（**谁说了算、规则是什么**）  
6. **`22-executive-dashboard/README.md`**（**一眼判断健康度**）  
7. **`17-execution-roadmap/README.md`**（**公司怎么做完**）  
8. **`20-product-iteration/README.md`**（**怎么持续迭代**）  
9. **`13-positioning-competition/00-Why-you-will-win-总纲.md`**  
10. **`24-brand-narrative/README.md`**（**用户听得懂、信得过、愿意传** — 与 **13** 理性论证互补）  
11. **`14-ux-conversion/01-转化漏斗-Visit到Escrow.md`**  
12. **`15-data-decision/README.md`**（勿与 **`spec/15`** 混淆）  
13. **`25-ecosystem-partnerships/README.md`**、**`26-endgame-strategy/README.md`**（VC：**产品还是生态**、**钱从哪退出**）— 正本含 **`25/05`～`07`**（钱与推进）、**`26/05`～`07`**（集中度 / 买家 / Token 行为）、落地 **`18/05`**  
14. **`23-scaling-playbook/README.md`**（多城复制前）  
15. **`18-operations-strategy/`**、**`19-risk-operations/`**（实战运营 + 异常闭环）  
16. **`09`～`12`、`16`** 按融资/合规节奏插入  
17. **`06-delivery-release/00-发布就绪桥接-spec-15-33-go-live.md`**（**`spec/15`** = 发版附录〇）

### B. VC / 资本侧速览

`22`（北极星与 KPI 树）→ **`24`**（一句话心智）→ `13` → **`25`**（生态）→ **`26`**（终局/退出）→ `11` → `16` → `05-go-to-market/01-Data-Room` → **`spec/01`、`08-4`、`82`～`84`**。

### C. 增长负责人

**`21`**（与风控/收入拉扯的规则）↔ **`24`**（传播母本）↔ `10`（机制）↔ **`18`**（SOP 落地）↔ **`23`**（封包复制）↔ **`25`**（伙伴导流）↔ **`14`**（转化）↔ **`15`**（决策与实验）↔ **`07`**（埋点与复盘）↔ **`22`**（经营看板）。

### D. 运营 / 客服负责人

**`19-risk-operations/`** ↔ **`16-regulation-risk/`** ↔ **`ops/RUNBOOK.md`**。

## 维护规则（企业级）

- **违规成本**：违反 **R1～R6**、**Impact Map**、**spec 先于上线** 等，一律按 **`01` §2.5** 处理；**当场谁执行、何时记 log** 见 **§2.5.1** 与 **`_registry/违规记录.md`**。  
- **会议执行**：规则须在会里卡点，见 **`08/meetings/01-Meeting-OS-规则与会议绑定.md`**（**§1.2** 需求评审 **三步** + **§1.1** 当场记 **`违规记录`**）；**权限矩阵**见 **`_registry/权限边界-强执行.md`**；**规则→人**见 **`_registry/规则绑定与执行责任.md`**；**每日**见 **`_registry/执行检查清单-每日版.md`**；**Office 是否在跑**见 **`_registry/Office运行健康度-System-Health-周检.md`**；**决策是否失真**见 **`21-product-operating-system/07-决策复盘机制-Decision-Review.md`**；**周会议程顺序**见 **`08/cadence/00` §2.1**（**22→15→21→新需求**）。  
- **灰度**：`spec` 未覆盖仍要上线 → **仅**允许 **`01` §2.4**；**反官僚**：**`_registry/反官僚原则.md`**。  
- 本目录内文档变更须在 **`_registry/版本登记与责任人模板.md`** 留痕（或等价变更记录）。
- 涉及 **数字、费用分母、收益路径、对外措辞** 的修改：**必须先改 `spec/` 中已定稿文档并走完治理联动**（如 **`scripts/check-governance-doc-linkage`**），再更新本 Office 叙述。
- **工程发版宣称**：以 **`spec/15-多维度文档与技术检查报告.md` 附录〇**、`go-live-checklist.md`、`spec/缺口与待补-官方总表.md` 为真值；**勿**与 **`15-data-decision/`** 目录名混谈「15」不写全路径。  
- **跨模块变更**：PRD / 叙事 / SOP 须带 **输入自 / 输出至 / Impact Map**（见 **`02-系统联动规则与模块Impact-Map.md`**）；各支柱 README 已链至对应 **§4.x** 锚点。  
- **15 日冲刺 Day15 终检**：**`99-real-world-validation/06-Day15-终检与证据索引-DD就绪.md`** + **`_registry/D15-终检与冲刺总结.md`** + **`PM-15` §B rg** + **`appendices/A-文档树-ASCII.txt`** + **`PM-MASTER-CHECKLIST…` §8.1** 一并过。  
- **编号防呆**：Office **`17`～`20`** 与 **`spec/17`（MVP清单）、`spec/18`（架构图）、`spec/19`（Escrow参数）、`spec/20`（云架构）** 同名不同义；Office **`21`～`23`** 与 **`spec/21`（UI3D）、`spec/22`（Design Tokens）、`spec/23`（UI 交付物/Figma）** 同名不同义；Office **`24`～`26`** 与 **`spec/24`（文档整理结论）、`spec/25`（顶级UI标准）、`spec/26`（文档审计报告）** 同名不同义；Office **`99-real-world-validation`** **不得** 与 **`spec/27-P*`** 阶段实现记录混称「27」—— 会议与工单 **必须写全路径**。

**文档 Owner**：产品负责人；**冲突时以 `spec/` 为准**。
