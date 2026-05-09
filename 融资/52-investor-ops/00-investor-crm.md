# 00 — Investor CRM（字段与阶段）

## 阶段枚举（与 `12` 一致）

`Research` → `Intro` → `FirstCall` → `DeepDive` → `Partner` → `IC` → `DD` → `TS` → `Close`

## 每条记录必填字段

| 字段 | 说明 |
|------|------|
| fund |  |
| partner |  |
| stage | 上表枚举 |
| next_action | 动词 + 日期 |
| deck_version_sent | 例 v3.2 |
| data_room_subset | 链接或文件夹名 |
| concerns | Partner 原话摘要 |
| champion_score | 1–5 |
| conflict_flag | 竞品组合 / 利益冲突 |

## 工具

- 可 **Airtable / Notion / HubSpot** — 本文件为 **字段契约**，避免三处各记一份。

---

**Owner**：CEO  
