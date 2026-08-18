---
name: msds-translator
description: Translates Chinese MSDS documents into professional English following the SUN-NOA standardized 16-section GHS MSDS template. Use when the user provides a Chinese MSDS (Word, PDF, or text) and asks for an English translation formatted according to the company's standard MSDS template.
---

# MSDS Translator

## Purpose
Translate Chinese MSDS (Material Safety Data Sheet) documents into professional English, outputting them in the SUN-NOA standardized 16-section GHS format.

## Required Inputs
- A Chinese MSDS document (Word, PDF, or pasted text)

## Process
1. Extract all text from the Chinese MSDS
2. Translate section by section into English
3. Map the content into the 16-section GHS template (see templates/MSDS-template.md)
4. Apply consistent industry terminology (see glossary.md)
5. Flag any missing or uncertain data with [bracketed placeholders]

## Output Format
- Follow the structure in templates/MSDS-template.md exactly
- Keep the fixed company information (SUN-NOA details) as-is
- Fill in product-specific data for each section
- Use [brackets] for any information not provided in the source document
- Follow Standard GHS section order: Section II = Hazards Identification, Section III = Information on Composition

## Terminology Rules
- Always refer to glossary.md for standardized terminology
- Use "Not available" for 无数据 (not "No data")
- Use "Boiling point" for 沸点
- Use "Dry powder" for 干粉
- If a term is not in the glossary, translate it literally and flag it with a note to review

## Content Rules
- Do NOT add content that is not in the source document
- Translate faithfully — do not interpret or embellish
- Flag any missing or uncertain data with [bracketed placeholders]
- If the source has fewer than 16 sections, fill missing sections with standard text or placeholders
- If a company name appears that is not SUN-NOA, flag it with a note to confirm

## Style Rules
- Professional, concise, descriptive tone
- Accurate industry terminology
- Consistent spelling (US English)
- No literal word-for-word translation
- Highlight certifications and hazard information clearly

## Template Reference
- Use templates/MSDS-template.md as the output structure
- Use glossary.md for standardized terminology
