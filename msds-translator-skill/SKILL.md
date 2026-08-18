# MSDS Translator

## Purpose
Translate Chinese MSDS (Material Safety Data Sheet) documents into professional English, outputting them in the SUN-NOA standardized 16-section GHS format.

## Input Required
- A Chinese MSDS document (Word, PDF, or pasted text)

## Process
1. Extract all text from the Chinese MSDS
2. Translate section by section into English
3. Map the content into the 16-section GHS template (see templates/MSDS-template.md)
4. Apply consistent industry terminology
5. Flag any missing or uncertain data with [bracketed placeholders]

## Output Format
- Follow the structure in templates/MSDS-template.md exactly
- Keep the fixed company information (SUN-NOA details) as-is
- Fill in product-specific data for each section
- Use [brackets] for any information not provided in the source document

## Style Rules
- Professional, concise, descriptive tone
- Accurate industry terminology
- Consistent spelling (US English)
- No literal word-for-word translation
- Highlight certifications and hazard information clearly

## Template Reference
- Use templates/MSDS-template.md as the output structure
