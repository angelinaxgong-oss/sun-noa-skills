# MSDS Format Specification (docx)

This file defines the exact formatting for all generated MSDS Word documents.
Always follow these values when producing a .docx output.

## 1. Page Setup
- Page size: Letter (11906 x 16838 twips = 8.5 x 11 inch)
- Margins (twips): top=1361, right=751, bottom=884, left=1785
- Header distance: 688, Footer distance: 716

## 2. Fonts
- Default body font: Arial, 10.5pt (sz=21)
- Composition table font: Helvetica Neue, 9.5pt (sz=19)

## 3. Title ("SAFETY DATA SHEET")
- Font: Arial, 21.5pt (sz=43), bold
- Alignment: centered
- Letter spacing: 0.6pt
- Spacing before: ~6pt

## 4. Product Name (e.g., "MS-8300")
- Font: Arial, 15.5pt (sz=31), bold
- Alignment: centered

## 5. Section Headings (e.g., "SECTION I: ...")
- Font: Arial, bold (same as body, bold)
- Style: BodyText
- Small left indent (~29 twips)
- Spacing before: ~57 twips

## 6. Body Text
- Font: Arial, 10.5pt (sz=21)
- Style: BodyText
- Line spacing: ~200 twips auto
- Black color (000000)

## 7. Tables (Composition / Physical Properties)
- Font: Helvetica Neue, 9.5pt (sz=19)
- Table width: 4550 twips (composition, 3 columns)
- Borders: none (no visible borders)
- Header row: not bold

## 8. Header (repeating on every page)
- Format: 2-column table (total width 9354 twips)
- Row 1 (no border):
  - Left: "Product Name：[Product Name]"
  - Right: "Date of issue: [Date]"
- Row 2 (bottom border, single, sz=4):
  - Left: "Supplier: Beijing SUN-NOA Technology Development Co., Ltd."
  - Right: "Date of revision: [Date]"
- Font: 9pt

## 9. Footer (repeating on every page)
- Content: page number (auto PAGE field)
- Font: 9pt (sz=18)
- Alignment: right

## 10. Fixed Content (always identical)
- Company info (Section I)
- Disclaimer (Section XVI)
- Other instructions (Section XVI)
