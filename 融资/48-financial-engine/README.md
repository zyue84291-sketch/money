# 48 — Financial Reality Layer（财务真值引擎）

**定位**：VC 对 **PPT 财务** 免疫；本目录规定 **模型结构、假设登记、版本号**，与 **[`02`](../02-经营真值-指标与财务-骨架.md)** 双签数字同源。

## 工作簿交付形态

| 规格文件 | Excel 工作簿名（团队自建） | 用途 |
|----------|---------------------------|------|
| [`00-burn-rate-model-SPEC.md`](./00-burn-rate-model-SPEC.md) | `00-burn-rate-model.xlsx` | 月度现金消耗 |
| [`01-runway-analysis-SPEC.md`](./01-runway-analysis-SPEC.md) | `01-runway-analysis.xlsx` | 跑道月数、融资触发 |
| [`02-token-liquidity-pressure-SPEC.md`](./02-token-liquidity-pressure-SPEC.md) | `02-token-liquidity-pressure.xlsx` | 解锁、抛压、MM（若适用） |
| [`03-treasury-risk-model-SPEC.md`](./03-treasury-risk-model-SPEC.md) | `03-treasury-risk-model.xlsx` | 金库集中度、稳定币风险 |
| [`04-scenario-simulation-SPEC.md`](./04-scenario-simulation-SPEC.md) | `04-scenario-simulation.xlsx` | Base / Downside / Stress |

**说明**：Git 仓库中 **不强制** 提交 `.xlsx`（可用 `.gitignore` 忽略）；**VDR Finance** 放 **只读导出 + 模型文件**；本目录 **SPEC + CSV 模板** 保证任何人能重建模型骨架。

## CSV 模板（可直接用 Excel 打开再另存为 xlsx）

- [`templates/monthly_actuals_template.csv`](./templates/monthly_actuals_template.csv)

**版本**：`model_version`：________ · **Owner**：CFO  
