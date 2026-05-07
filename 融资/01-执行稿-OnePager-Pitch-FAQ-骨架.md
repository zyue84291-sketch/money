# 01 — 执行稿：One Pager · Pitch · FAQ（骨架）

**用途**：路演与首次触达用的 **短材料**；正文维护在主仓库 **`product-manager/`**。

## SSOT（勿在本夹重复写长文）

| 材料 | 路径 |
|------|------|
| One Pager | [`../TT-Expedition-docs/product-manager/25-项目 One Pager（对外初稿）.md`](../TT-Expedition-docs/product-manager/25-项目 One Pager（对外初稿）.md) |
| FAQ | [`../TT-Expedition-docs/product-manager/26-项目 FAQ（对外初稿）.md`](../TT-Expedition-docs/product-manager/26-项目 FAQ（对外初稿）.md) |
| Pitch 页序 | [`../TT-Expedition-docs/product-manager/27-Pitch Deck 初稿（页序版）.md`](../TT-Expedition-docs/product-manager/27-Pitch Deck 初稿（页序版）.md) |
| 一级市场清单（可选） | [`../TT-Expedition-docs/product-manager/12-一级市场与融资渠道清单.md`](../TT-Expedition-docs/product-manager/12-一级市场与融资渠道清单.md) |

## 本夹可放的「派生物」（可选）

- [ ] `exports/` 目录：导出 PDF 的说明（**不提交**敏感 PDF 时，只写「生成日期 + 对应 commit」）  
- [ ] 一页「**本次会面版本**」：日期、听众、**禁止口头扩展**的边界 bullet

## 撰写检查（对外前打勾）

- [ ] 数字与 **`spec/08-4`**、**`09/00` §0** 已核对  
- [ ] Token / 治理相关表述已与 **`spec/82`～`84`** 或法务占位一致  
- [ ] 已读 **`05-go-to-market/00`** 材料门禁  

---

## 企业级填充（PM · 一级市场材料包）

**产品名**：**TravelTrust** — 链上 **USDC Escrow + 可验证状态机** 完成「付款—履约—争议—结算」；撮合与规模化运营在链下（**`spec/01`** 混合架构）。

### 对外材料「三层栈」（勿混写）

| 层 | 内容 | 主仓库入口 |
|----|------|------------|
| **L1 执行稿** | One Pager / FAQ / Deck 页序 | `product-manager/25`、`26`、`27` |
| **L2 资本叙事** | VC 六件套、TAM、Why now、Use of Funds、Investment Trigger | `product-management-office/11-capital-narrative/README.md` |
| **L3 真值** | 指标、费用、对外禁语 | **`spec/08-4`**、**`09-business-model/00` §0**、**`11/06`** |

### Deck 建议页序（与 Office「VC 速览」一致）

1. 一句话 + 为什么现在（**`11/01`**）  
2. 问题：Trust / Fraud / Payment（同上）  
3. 方案与混合架构（**`11/02`** + **`spec/01`** 指针）  
4. Traction（**仅引用 `09/00` §0** 已签数字）  
5. 市场 TAM/SAM/SOM（**`11/00`**，页脚 `doc_version`）  
6. Why you win（摘要 → **`13/00`**）  
7. 商业模式与单位经济（**`09`**）  
8. 增长与第二城（**`10`**、**`23`**）  
9. 合规边界一句（**`16/00` Top Narrative**）  
10. 团队 + 融资条款占位  

### FAQ 必背（机构高频）

| 问题 | 回答落点 |
|------|----------|
| 你们是持牌托管吗？ | **`16/00` §3** 法律定性；**不**自称银行存款机构直至法务书面 |
| Escrow 与收入关系？ | **`09/05`** Revenue≠Cash；GMV 与 Net Rev 定义 |
| 链上证据在哪？ | **`spec/01` §10**、索引器 **`spec/110`**、对账 **`09/05`** |
| 为什么不用纯 OTA？ | **`13/02`** 替代方案 |
| Token？ | **`26/00` 披露门禁**；无发行则 Deck 删环 |

### 会议卡（每次会面填写）

| 日期 | 听众类型 | Deck `doc_version` | 口头未承诺事项 |
|------|-----------|-------------------|------------------|

---

**Owner**：PM-O（联席：CEO / 增长负责人）  
**更新日期**：2026-05-08
