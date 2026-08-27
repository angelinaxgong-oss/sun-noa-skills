---
name: water-based-tds-translator
description: Translates Chinese water-based adhesive TDS (Technical Data Sheet) documents — including single-component (1K) PVAc/D3 and two-component (2K) EPI/D4 products — into professional English following the SUN-NOA standardized TDS template, and produces standardized Chinese versions as well. Use when the user provides a Chinese water-based adhesive TDS or specification and asks for a technical data sheet in English or Chinese.
---

# Water-based TDS Translator

## Purpose
Translate Chinese water-based adhesive TDS documents into professional English following the SUN-NOA standardized TDS format, and produce standardized Chinese (CN) versions. Supports both single-component (1K) and two-component (2K / EPI) products.

## Required Inputs
- A Chinese water-based adhesive TDS or product specification (Word, PDF, or pasted text)
- Product name (and English product name if different)
- Product type: single-component (1K) or two-component (2K / EPI)

## Process
1. Extract all text from the Chinese water-based TDS
2. Translate into English (or format into Chinese for CN output)
3. Map the content into the water-based TDS template structure
4. Apply water-based terminology (see glossary.md)
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
6. Cleaning / 清洁 — KEEP this section (water-based products include cleaning instructions)
7. Shelf Life / 保质期 — ALWAYS leave blank for manual input
8. Packaging / 包装 — ALWAYS leave blank for manual input
9. Disclaimer / 免责声明 — placed at the BOTTOM of the body

## Product Types (1K vs 2K)
This skill handles BOTH product types:
- **Single-component (1K)** — e.g., PVAc D3 adhesives. No mixing ratio or pot life.
- **Two-component (2K / EPI)** — e.g., EPI D4 adhesives (main agent + hardener). Has mixing ratio and pot life.

The same fixed-field lists below are used for both. The rule "omit any field NOT in the source" automatically drops the 2K-only fields for 1K products.

## Technical Specification — FIXED fields (water-based, CORE)
Extract these fields from the source. If a field is NOT provided in the source, omit it entirely (remove the row — do NOT add a placeholder):
| EN | CN |
|---|---|
| Appearance | 外观 |
| Base / Polymer type | 基体 / 聚合物类型 |
| Solid content | 固含量 / 总固体含量 |
| Viscosity | 粘度 |
| pH | pH值 |
| Toxicity | 毒性 |

## Technical Specification — FIXED fields (2K / EPI ONLY)
These fields apply ONLY to two-component (EPI) products. For single-component (1K) products they are not in the source and are therefore omitted:
| EN | CN |
|---|---|
| Mixing ratio (by weight) | 配比（重量比） |
| Pot life | 适用期 |
| MFFT (minimum film-forming temperature) | MFFT（最低成膜温度） |

## Waterproof Grade (D3/D4) — goes in Characteristics, NOT the spec table
- The DIN EN 204 waterproof grade (D3 / D4) and any environmental grade (e.g., F★★★★) are CHARACTERISTICS, not technical parameters. Place them in the Characteristics / 特点 section.

## Application Parameters — FIXED fields (water-based)
Extract these fields from the source. If a field is NOT provided in the source, omit it entirely (remove the row — do NOT add a placeholder):
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
- Waterproof grade (D3/D4) and environmental grade (F★★★★) belong in Characteristics, NOT the Technical Specification table
- Cleaning / 清洁 section is KEPT (do not delete). If the source has no cleaning instructions, mark [Not provided in source] / [源文件未提供]
- Precautions / 注意事项 section: include usage instructions, safety and storage from the source. If none is provided, mark [Not provided in source] / [源文件未提供]
- Shelf Life and Packaging must ALWAYS be left blank (with [To be completed] / [待填写] placeholder) for manual input
- If any other company name appears (e.g., OEM manufacturer), remove it entirely
- Only SUN-NOA company information should appear in the final document

## Terminology Rules
- Always refer to glossary.md for standardized water-based terminology
- If a term is not in the glossary, translate it literally and flag it with a note to review

## Style Rules
- Professional, concise, descriptive tone
- Accurate industry terminology
- Consistent spelling (US English for EN output)
- No literal word-for-word translation

## File References
- templates/TDS-template.md — English structure
- templates/TDS-template-cn.md — Chinese structure
- glossary.md — standardized CN↔EN water-based terminology
- format-spec.md — English docx formatting
- format-spec-cn.md — Chinese docx formatting
