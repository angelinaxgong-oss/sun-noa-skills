---
name: msds-translator
description: Translates Chinese MSDS documents into professional English following the SUN-NOA standardized 16-section GHS MSDS template. Use when the user provides a Chinese MSDS (Word, PDF, or text) and asks for an English translation formatted according to the company's standard MSDS template.
---

# MSDS Translator

## Purpose
Translate Chinese MSDS (Material Safety Data Sheet) documents into professional English, outputting them in the SUN-NOA standardized 16-section GHS format. Also supports producing a standardized Chinese (CN) version.

## Required Inputs
- A Chinese MSDS document (Word, PDF, or pasted text)

## Process
1. Extract all text from the Chinese MSDS
2. Translate section by section into English (or format into Chinese for CN output)
3. Map the content into the 16-section GHS template
4. Apply consistent industry terminology (see glossary.md)
5. Apply formatting (see format-spec.md / format-spec-cn.md)
6. Flag any missing or uncertain data with [bracketed placeholders]

## Output Language
This skill supports TWO output modes:
1. **Chinese (CN)** — output follows templates/MSDS-template-cn.md and format-spec-cn.md
2. **English (EN)** — output follows templates/MSDS-template.md and format-spec.md

When the user requests a Chinese output, use the CN template and CN format-spec.
When the user requests an English output, use the EN template and EN format-spec.
If the user requests both, produce both versions.

## Output Format
- Follow the 16-section GHS structure exactly (EN or CN as requested)
- Keep the fixed company information as-is (see Company Information below)
- Fill in product-specific data for each section
- Use [brackets] for any information not provided in the source document
- Follow Standard GHS section order: Section II = Hazards Identification, Section III = Information on Composition

## Company Information (fixed)
English:
- Company Name: Beijing SUN-NOA Technology Development Co., Ltd.
- Address: Room 504, Building 2, Tuqiao PLUS Cultural and Creative Industrial Park, Tongzhou District, Beijing, China
- Phone: +86-10-85365010
- Fax: +86-10-85365010
- Emergency Contact: +86-10-85365010 / +86-13910612601

Chinese (中文):
- 公司名称：北京圣诺亚科技发展有限公司
- 地址：北京市通州区土桥PLUS文创产业园2号楼504室
- 电话：+86-10-85365010
- 传真：+86-10-85365010
- 应急电话：+86-10-85365010 / +86-13910612601

## Format Rules
- Always apply the formatting defined in the relevant format-spec file:
  - EN output: format-spec.md (font Arial 10.5pt)
  - CN output: format-spec-cn.md (font 宋体 SimSun 10.5pt, 西文 Times New Roman)
- Line spacing: 1.5 (w:line=360)
- Title: 21.5pt bold centered
- Product name: 15.5pt bold centered
- Section headings: 15.5pt bold
- Header: 2-column table (Product Name / Date of issue, Supplier / Date of revision)
- Footer: page number, 9pt, right-aligned
- Empty line between sections

## Terminology Rules
- Always refer to glossary.md for standardized terminology
- Use "Not available" (EN) / "无数据" (CN) for 无数据
- Use "Boiling point" (EN) / "沸点" (CN) for 沸点
- Use "Dry powder" (EN) / "干粉" (CN) for 干粉
- If a term is not in the glossary, translate it literally and flag it with a note to review

## Content Rules
- Do NOT add content that is not in the source document
- Translate faithfully — do not interpret or embellish
- Flag any missing or uncertain data with [bracketed placeholders]

## Section Completion Rules (for each section, in order of priority)
1. If the source PROVIDES content for a section → translate it faithfully and use it
2. If the source does NOT have that section, or it is empty → use the default fallback text
3. Never overwrite source content with default text

## Default Fallback Text (ONLY when source is missing/empty)
- Section XII (Ecological / 生态学信息): "No data available." / "无有关数据"
- Section XIV (Transport / 运输信息): "Not classified as dangerous goods." / "非危险货物"
- Section XV (Regulatory / 法规信息): "Not classified as hazardous chemical according to applicable regulations." / "根据适用法规，不属于危险化学品"

## Company Name Rules
- The only company names that may appear are:
  - English: Beijing SUN-NOA Technology Development Co., Ltd.
  - Chinese: 北京圣诺亚科技发展有限公司
- If any other company name appears (e.g., an OEM manufacturer), remove the company name and any sentence containing it entirely — do NOT translate it, do NOT flag it

## Style Rules
- Professional, concise, descriptive tone
- Accurate industry terminology
- Consistent spelling (US English for EN output)
- No literal word-for-word translation
- Highlight certifications and hazard information clearly

## File References
- templates/MSDS-template.md — English 16-section structure
- templates/MSDS-template-cn.md — Chinese 16-section structure
- glossary.md — standardized CN↔EN terminology
- format-spec.md — English docx formatting
- format-spec-cn.md — Chinese docx formatting
