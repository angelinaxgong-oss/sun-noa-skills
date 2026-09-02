---
name: tds-translator
description: Translates Chinese adhesive TDS (Technical Data Sheet) documents — EVA hot melt, PUR hot melt, and water-based (single-component 1K and two-component 2K/EPI) adhesives — into professional English following the SUN-NOA standardized TDS template, and produces standardized Chinese versions as well. Use when the user provides a Chinese adhesive TDS or specification and asks for a technical data sheet in English or Chinese.
---

# TDS Translator (Unified)

## Purpose
Translate Chinese adhesive TDS documents into professional English following the SUN-NOA standardized TDS format, and produce standardized Chinese (CN) versions. Supports all adhesive types: EVA hot melt, PUR hot melt, and water-based (single-component 1K and two-component 2K / EPI).

## Required Inputs
- A Chinese adhesive TDS or product specification (Word, PDF, or pasted text)
- Product name (and English product name if different)
- Product type — the user will state it:
  1. EVA hot melt
  2. PUR hot melt
  3. Water-based single-component (1K)
  4. Water-based two-component (2K / EPI)

## Process
1. Extract all text from the Chinese TDS
2. Translate into English (or format into Chinese for CN output)
3. Map content into the unified TDS template
4. Apply the type-specific fixed spec fields (below)
5. Apply terminology (see glossary.md)
6. Apply formatting (see format-spec.md / format-spec-cn.md)
7. Flag missing or uncertain data with [bracketed placeholders]

## Output Language
Two output modes:
1. **English (EN)** — templates/TDS-template.md + format-spec.md
2. **Chinese (CN)** — templates/TDS-template-cn.md + format-spec-cn.md

When the user requests English output, use the EN template and EN format-spec.
When the user requests Chinese output, use the CN template and CN format-spec.
If the user requests both, produce both versions.

## Output Structure (7 sections + disclaimer)
1. Product Description / 产品描述
2. Characteristics / 特点
3. Technical Specification / 技术参数
4. Application Parameters / 施工参数
5. Precautions / 注意事项 — contains fixed subsections: Safety (安全事项), Storage (储存), Cleaning (清洁)
6. Shelf Life / 保质期 — ALWAYS leave blank ([To be completed] / [待填写])
7. Packaging / 包装 — ALWAYS leave blank ([To be completed] / [待填写])
- Disclaimer — fixed text at the bottom

## Technical Specification — FIXED fields by type
Use the list matching the stated product type. If a field is NOT provided in the source, omit it entirely (remove the row — do NOT add a placeholder).

### EVA hot melt
| EN | CN |
|---|---|
| Appearance | 外观 |
| Melt Viscosity (Brookfield, @200°C) | 熔融粘度（Brookfield，@200℃） |
| Softening Point (Ring & Ball) | 软化点（环球法） |
| Density | 密度 |

### PUR hot melt
| EN | CN |
|---|---|
| Appearance | 外观 |
| Viscosity | 粘度 |
| Solid content | 固含量 |
| Density | 密度 |
| Open time | 开放时间 |

### Water-based (1K & 2K)
| EN | CN |
|---|---|
| Appearance | 外观 |
| Base / Polymer type | 基体 / 聚合物类型 |
| Solid content | 固含量 / 总固体含量 |
| Viscosity | 粘度 |
| pH | pH值 |
| Toxicity | 毒性 |
| Mixing ratio (by weight) | 配比（重量比） — 2K only |
| Pot life | 适用期 — 2K only |
| MFFT (minimum film-forming temperature) | MFFT（最低成膜温度） — 2K only |

## Application Parameters — FIXED fields by type
If a field is NOT provided in the source, omit it entirely (remove the row — do NOT add a placeholder).

### EVA hot melt
| EN | CN |
|---|---|
| Material moisture content | 材料含水率 |
| Ambient temperature | 环境温度 |
| Material temperature | 材料温度 |
| Glue tank temperature | 胶槽温度 |
| Glue roller temperature | 涂胶辊温度 |
| Press roller pressure | 压辊压力 |
| Feed speed | 进料速度 |
| Application amount | 涂胶量 |

### PUR hot melt
| EN | CN |
|---|---|
| Press plate temperature | 压盘温度 |
| Glue tube temperature | 胶管温度 |
| Scraper temperature | 刮刀温度 |
| Application amount | 涂胶量 |
| Feed speed | 进料速度 |
| Material temperature | 材料温度 |

### Water-based
| EN | CN |
|---|---|
| Application amount | 涂胶量 |
| Open time | 开放时间 |
| Pressure | 压力 |
| Pressing time | 加压时间 |
| Working temperature | 使用温度 / 最佳使用温度 |
| Minimum working temperature | 最低工作温度 |
| Substrate moisture content | 基材含水率 |
| Application method | 涂胶方式 |

## Cleaning Methods by Type
Used for the Cleaning (清洁) subsection inside Precautions (注意事项): use the source's cleaning method if provided; otherwise use the standard method below for the product type.

| Type | Cleaning method (CN) | Cleaning method (EN) |
|---|---|---|
| EVA hot melt | 推荐使用专用的清洗剂清洗与胶水相接触的应用单元。 | It is recommended to use a dedicated cleaner to clean the application units that come into contact with the adhesive. |
| PUR hot melt | 若停机时间过长，推荐使用专用的清洗剂清洗与胶水相接触的应用单元，以免胶水交联固化，对设备产生危害。 | If the machine is shut down for an extended period, it is recommended to use a dedicated cleaner to clean the application units that come into contact with the adhesive, so as to prevent the adhesive from crosslinking and curing, which could damage the equipment. |
| Water-based (1K/2K) | 胶水未干燥前用清水清洗工具和机器。 | Clean tools and machines with clean water before the adhesive dries. |
| MS polymer | 未固化前用布擦拭，并用酒精或矿物油精擦净；已固化的密封胶只能机械清除（切割/刮除），溶剂无法溶解；使用后密封胶嘴。 | Wipe with a cloth before curing, and clean with alcohol or mineral spirits; once cured, the sealant can only be removed mechanically (cutting/scraping) — solvents will not dissolve it; seal the nozzle after use. |

Note: Always end the cleaning subsection with one more line after the method above: "或咨询我司技术部。" (EN: "Or consult our technical department.")

## Fixed Safety Statements (apply to ALL TDS)
The following two statements are ALWAYS included under the Safety (安全事项) subsection inside Precautions (注意事项), regardless of product type:

1. CN: 使用和处理本产品时请参照MSDS或咨询我司技术部。
   EN: When using and handling this product, refer to the MSDS or consult our technical department.
2. CN: 批量使用前，请先行在线小试评估。
   EN: Before batch application, please first conduct a small-scale on-line trial evaluation.

## Company Information (fixed — used in the header)
English:
- Company Name: Beijing SUN-NOA Technology Development Co., Ltd.
- Tel/Add: Tel: +86-10-85365010 Add：Room 504, Building 2, Tuqiao PLUS  Tongzhou District, Beijing China

Chinese (中文):
- 公司名称：北京圣诺亚科技发展有限公司
- 电话/地址：电话：+86-10-85365010 地址：北京市通州区土桥PLUS文创产业园2号楼504室

## Format Rules
- Always apply the formatting defined in the relevant format-spec file:
  - EN output: format-spec.md (font Arial 10.5pt)
  - CN output: format-spec-cn.md (font 宋体 SimSun 10.5pt, 西文 Times New Roman)
- Title block (CENTERED): "Technical Data Sheet" / "技术数据表" (14pt bold) above the product name (15.5pt bold)
- Header: ONLY two centered lines (company name + Tel/Add), 9pt
- Footer: page number, right-aligned, 9pt
- Line spacing: 1.5 (w:line=360)
- Empty line between sections

## Content Rules
- Do NOT add content that is not in the source document
- Translate faithfully — do not interpret or embellish
- Product Description (产品描述) must state what the product IS and what it is USED FOR. If the source's description is very short, expand it by drawing on information elsewhere in the document (application fields, product type, characteristics) — do NOT invent new facts, only consolidate what the source already states
- Top-level section names are FIXED. CN output must use these exact names in this order: 产品描述 / 特点 / 技术参数 / 施工参数 / 注意事项 / 保质期 / 包装. Always rename source synonyms to these (e.g., 产品规格 → 技术参数, 应用领域 → 产品描述). Subsections INSIDE 注意事项 are flexible (their names follow the source)
- Fixed spec / application-parameter fields NOT in the source must be OMITTED (remove the row entirely — do NOT add a [Not provided] placeholder)
- Safety (安全事项), Storage (储存) and Cleaning (清洁) are subsections INSIDE Precautions (注意事项), NOT separate top-level sections. Their subsection names are flexible and may follow the source wording
- Cleaning (清洁) is a FIXED subsection inside Precautions (注意事项). If the source provides a cleaning method, use the source's; if not, insert the standard cleaning method for the product type (see Cleaning Methods by Type below). Always end the cleaning subsection with one more line: "或咨询我司技术部。" (EN: "Or consult our technical department.")
- Waterproof grade (D3/D4, DIN EN204) and environmental grade (F★★★★) belong in Characteristics, NOT the Technical Specification table
- Shelf Life and Packaging must ALWAYS be left blank ([To be completed] / [待填写]) for manual input
- If any other company name appears (e.g., OEM manufacturer), remove it entirely
- Only SUN-NOA company information should appear in the final document

## Terminology Rules
- Always refer to glossary.md for standardized terminology
- Use "Not available" (EN) / "无数据" (CN) for 无数据 (when a value must still be shown)
- If a term is not in the glossary, translate it literally and flag it with a note to review

## Style Rules
- Professional, concise, descriptive tone
- Accurate industry terminology
- Consistent spelling (US English for EN output)
- No literal word-for-word translation

## File References
- templates/TDS-template.md — English structure
- templates/TDS-template-cn.md — Chinese structure
- glossary.md — standardized CN↔EN terminology
- format-spec.md — English docx formatting
- format-spec-cn.md — Chinese docx formatting
