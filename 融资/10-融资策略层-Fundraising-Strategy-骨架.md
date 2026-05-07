# 10 — 融资策略层（Fundraising Strategy）

**用途**：从「有材料」升级为「有打法」——明确 **本轮要什么钱、凭什么估值、怎么稀释、用什么工具、按什么节奏**；与 Deck 叙事分离：**策略是内部决策文档**，对外只输出一致口径。

## SSOT（与主仓库对齐）

| 主题 | 路径 |
|------|------|
| 资本叙事与数字对齐 | [`../TT-Expedition-docs/product-management-office/11-capital-narrative/`](../TT-Expedition-docs/product-management-office/11-capital-narrative/) |
| 终局 / 价值捕获（勿与本轮条款混写） | [`../TT-Expedition-docs/product-management-office/26-endgame-strategy/`](../TT-Expedition-docs/product-management-office/26-endgame-strategy/) |
| 合规边界（证券/Token 表述） | [`../TT-Expedition-docs/product-management-office/16-regulation-risk/`](../TT-Expedition-docs/product-management-office/16-regulation-risk/)（若存在） |
| 对外叙事门禁 | [`../TT-Expedition-docs/product-management-office/05-go-to-market/00-对外叙事与材料门禁-082-084-08-4.md`](../TT-Expedition-docs/product-management-office/05-go-to-market/00-对外叙事与材料门禁-082-084-08-4.md) |

---

## 1. 融资轮设计（Round Design）

**要写清**：本轮名称（Pre-seed / Seed / A）、**金额区间**、**主要用途拆分**（产品/增长/合规/储备金）、**达标里程碑**（与下一轮融资触发条件挂钩）。

- [ ] **本轮目标金额**（硬下限 / 理想 / 可接受的 oversubscribe 上限）已书面化  
- [ ] **资金用途** 与 `11/` 资本叙事、财务模型 **同一套数字**  
- [ ] **下一轮融资假设**（时间、关键指标门槛）已写 1 页，避免「本轮故事」与「下一轮故事」打架  

---

## 2. 估值逻辑（Valuation Logic）

**要写清**：可比法（Comps）、DCF/回报倒推（机构常用）、**关键假设**（渗透率、Take rate、协议收入）、**敏感性表**（最好/基准/压力）。

- [ ] **估值区间** 与 **稀释上限** 已联立（见 §3）  
- [ ] Deck 里只保留 **1 条主逻辑**；详细假设进 Data Room / 模型表  
- [ ] 与 **`11/06`**、**`22/07`** 口径 **可对拍**  

---

## 3. 稀释模型（Dilution Model）

**要写清**：本轮前 fully diluted、**option pool refresh**、SAFE 堆叠、**本轮后 cap table 情景**（最小融资 / 目标 / 超募）。

- [ ] **创始人合计稀释** 与 **单轮上限** 已设红线（董事会/股东协议前置思考）  
- [ ] 若用 SAFE：**估值帽 / 折扣 / MFN** 组合对 **未来 priced round** 的影响已表格化  
- [ ] **ESOP** 是否本轮扩大、与招聘计划的 **时间匹配**  

---

## 4. SAFE / Equity / Token 选择（Instrument Choice）

**要写清**：地理与投资人结构下的 **默认工具**、**为何不选其他**、**Token 权利是否与股权解耦**（法律审阅后定稿）。

| 工具 | 典型适用 | 本项目的决策（待填） |
|------|-----------|----------------------|
| SAFE / 可转债 | 速度快、条款标准化程度高 | |
| Priced equity | 机构主导、cap table 清晰 | |
| Token warrant / SAFT 类（若适用） | 需极强合规与披露；多数机构单独审 | |
| 纯协议层 Token（无募资） | 与融资条款分离时的叙事 | |

- [ ] **律师已确认** 对外表述与 **实际签署文件** 一致（无「Deck 有 Token 募资、合同无」类 Red flag）  
- [ ] **`13-cap-table-tokenomics`** 与本节 **同一结论**  

---

## 5. 融资时间线（Pre-seed → Seed → A）

**要写清**：**准备期**（材料/Data Room）→ **quiet / loud 窗口** → **first close** → **DD** → **final close**；每阶段的 **owner** 与 **退出标准**。

- [ ] 与 **`12-fundraising-operations`** 中的 CRM 阶段定义 **一致**  
- [ ] 重大产品/合规节点（主网、试点城市、审计）与 **路演窗口** 已对齐，避免「真空期密集见投资人」  

---

## 企业级填充（PM · 与 `11-capital-narrative` 同窗）

### Use of Funds（默认桶 — 与 Office README VC 六件套一致）

| 桶 | 比例（首稿） | 里程碑锚点（SSOT） |
|----|--------------|---------------------|
| 增长 | 40% | `09/00` §0 MAU/GMV；CAC `10/04` |
| 供给 | 30% | 活跃 Guide；**`23/04`** 第二城 |
| 技术 | 20% | 对账绿、P0 资金为零 — `06-delivery-release`、`19-risk-operations` |
| 合规 | 10% | **`16`** 矩阵绿灯 + **`08-4`** |

### 估值叙事素材（勿在本文写「拍脑袋倍数」）

- **可比与敏感性**：财务模型须与 **`09`**、**`11/00` TAM** 同源版本号。  
- **Moat 量化**：**`11/02` §5** + **`10/00` §5.1**。  
- **窗口句完整版**：**`11-capital-narrative/README.md` VC 六件套 §6**（与 **`09/06`** 排除条件同读）。

### 与主仓库冲突时的优先级

**`spec/` > 法务书面 > `09/00` §0 > 本夹策略笔记**。

---

**Owner**：CEO + CFO  
**更新日期**：2026-05-08
