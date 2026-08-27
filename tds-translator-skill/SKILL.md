---
name: tds-translator
description: Translates Chinese TDS (Technical Data Sheet) documents into professional English following the SUN-NOA standardized TDS template, and produces standardized Chinese versions as well. Use when the user provides a Chinese TDS or product specification and asks for a technical data sheet in English or Chinese.
---

# TDS Translator

## Purpose
Translate Chinese TDS (Technical Data Sheet) documents into professional English following the SUN-NOA standardized TDS format, and produce standardized Chinese (CN) versions. Supports both output languages.

## Required Inputs
- A Chinese TDS or product specification document (Word, PDF, or pasted text)
- Product name (and English product name if different)

## Process
1. Extract all text from the Chinese TDS
2. Translate into English (or format into Chinese for CN output)
3. Map the content into the TDS template structure
4. Apply consistent industry terminology (see glossary.md)
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
4. Application Techniques / 施工技术
5. Remark / 备注
6. Cleaning / 清洁
7. Shelf Life / 保质期 — ALWAYS leave blank for manual input
8. Packaging / 包装 — ALWAYS leave blank for manual input
9. Disclaimer / 免责声明

## Company Information (fixed)
English:
- Company Name: Beijing SUN-NOA Technology Development Co., Ltd.
- Address: Room 504, Building 2, Tuqiao PLUS Cultural and Creative Industrial Park, Tongzhou District, Beijing, China
- Phone: +86-10-85365010

Chinese (中文):
- 公司名称：北京圣诺亚科技发展有限公司
- 地址：北京市通州区土桥PLUS文创产业园2号楼504室
- 电话：+86-10-85365010

## Content Rules
- Do NOT add content that is not in the source document
- Translate faithfully — do not interpret or embellish
- Flag any missing or uncertain data with [bracketed placeholders]
- Shelf Life and Packaging must ALWAYS be left blank (with [To be completed] placeholder) for manual input
- If any other company name appears (e.g., OEM manufacturer), remove it entirely

## Terminology Rules
- Always refer to glossary.md for standardized terminology
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
