---
name: eva-tds-translator
description: Translates Chinese EVA hot melt adhesive TDS (Technical Data Sheet) documents into professional English following the SUN-NOA standardized TDS template, and produces standardized Chinese versions as well. Use when the user provides a Chinese EVA hot melt TDS or specification and asks for a technical data sheet in English or Chinese.
---

# EVA TDS Translator

## Purpose
Translate Chinese EVA hot melt adhesive TDS documents into professional English following the SUN-NOA standardized TDS format, and produce standardized Chinese (CN) versions. Supports both output languages.

## Required Inputs
- A Chinese EVA hot melt TDS or product specification document (Word, PDF, or pasted text)
- Product name (and English product name if different)

## Process
1. Extract all text from the Chinese EVA TDS
2. Translate into English (or format into Chinese for CN output)
3. Map the content into the EVA TDS template structure
4. Apply EVA-specific terminology (see glossary.md)
5. Apply formatting (see format-spec.md / format-spec-cn.md)
6. Flag any missing or uncertain data with [bracketed placeholders]

## Output Language
This skill supports TWO output modes:
1. **English (EN)** — output follows templates/TDS-template.md and format-spec.md
2. **Chinese (CN)** — output follows templates/TDS-template-cn.md and format-spec-cn.md

When the user requests English output, use the EN template and EN format-spec.
When the user requests Chinese output, use the CN template and CN format-spec.
If the user requests both, produce both versions.

## Output Structure (in order)
1. Application / 用途
2. Characteristics / 特点
3. Technical Specification / 技术参数
4. Application Parameters / 施工参数
5. Precautions / 注意事项 — usage instructions, safety, storage, etc.
6. Shelf Life / 保质期 — ALWAYS leave blank for manual input
7. Packaging / 包装 — ALWAYS leave blank for manual input
8. Disclaimer / 免责声明 — placed at the BOTTOM of the body

## Technical Specification — FIXED fields (EVA)
Extract these fields from the source. If a field is NOT provided in the source, omit it entirely (remove the row — do NOT add a placeholder):
| EN | CN |
|---|---|
| Appearance | 外观 |
| Melt Viscosity (Brookfield, @200°C) | 熔融粘度（Brookfield，@200℃） |
| Softening Point (Ring & Ball) | 软化点（环球法） |
| Density | 密度 |

## Application Parameters — FIXED fields (EVA)
Extract these fields from the source. If a field is NOT provided in the source, omit it entirely (remove the row — do NOT add a placeholder):
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

## Company Information (fixed)
English:
- Company Name: Beijing SUN-NOA Technology Development Co.,Ltd.
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
- Fixed spec / application-parameter fields NOT in the source must be OMITTED (remove the row entirely — do NOT add a [Not provided] placeholder)
- Precautions / 注意事项 section: include usage instructions, safety and storage from the source. If none is provided, mark [Not provided in source] / [源文件未提供]
- Shelf Life and Packaging must ALWAYS be left blank (with [To be completed] / [待填写] placeholder) for manual input
- If any other company name appears (e.g., OEM manufacturer), remove it entirely
- Only SUN-NOA company information should appear in the final document

## Terminology Rules
- Always refer to glossary.md for standardized EVA terminology
- If a term is not in the glossary, translate it literally and flag it with a note to review

## Style Rules
- Professional, concise, descriptive tone
- Accurate industry terminology
- Consistent spelling (US English for EN output)
- No literal word-for-word translation

## File References
- templates/TDS-template.md — English structure
- templates/TDS-template-cn.md — Chinese structure
- glossary.md — standardized CN↔EN EVA terminology
- format-spec.md — English docx formatting
- format-spec-cn.md — Chinese docx formatting
