# MSDS Format Specification (docx)

This file defines the EXACT formatting for all generated MSDS Word documents.
Always follow these values when producing a .docx output. Do not change unless the user says so.

## 1. Page Setup
- Page size: Letter (11906 x 16838 twips)
- Margins (twips): top=1361, right=751, bottom=884, left=1785
- Header distance: 688, Footer distance: 716

## 2. Fonts
- Default body font: Arial, 10.5pt (sz=21)
- Table font: Helvetica Neue, 9.5pt (sz=19)
- Header/footer font: 9pt (sz=18)

## 3. Line Spacing
- Body and headings: 1.5 line spacing (w:line=360, lineRule=auto)
- Table cells: w:line=300 (slightly tighter)

## 4. Title ("SAFETY DATA SHEET")
- Font: Arial, 21.5pt (sz=43), bold
- Alignment: centered
- Letter spacing: 0.6pt (w:spacing=12)
- Spacing before: 128

## 5. Product Name (e.g., "MS-8300")
- Font: Arial, 15.5pt (sz=31), bold
- Alignment: centered
- Spacing before: 92

## 6. Product Info Lines (Product Name / Issue Date / Revision Date)
- Bold label + regular value, Arial 10.5pt
- Spacing before: ~53-57
- Left indent: ~29-30

## 7. Section Headings ("SECTION I: ...")
- Font: Arial, 15.5pt (sz=31), bold
- Letter spacing: 0.5pt (w:spacing=10)
- Spacing before: 93
- Left indent: 21
- EMPTY LINE before every section (except the first)

## 8. Sub-headings ("COMPANY INFORMATION", "EMERGENCY OVERVIEW", etc.)
- Font: Arial, 10.5pt (sz=21), bold
- Spacing before: 57
- Left indent: 22

## 9. Body Text
- Font: Arial, 10.5pt (sz=21)
- Spacing before: 52
- Left indent: 29
- Label + value lines: bold label, regular value

## 10. Tables (Composition / Physical Properties)
- Font: Helvetica Neue, 9.5pt (sz=19)
- Table width: 4550 twips (composition: 3 cols = 2464/1419/667; properties: 2 cols = 2464/2086)
- Borders: none
- Header row: not bold

## 11. Header (repeating on every page)
- Format: 2-column table (total width 9354, cols = 5078 + 4276)
- Row 1 (no border):
  - Left: "Product Name：[Product Name]"
  - Right: "Date of issue: [Date]"
- Row 2 (bottom border, single, sz=4):
  - Left: "Supplier: Beijing SUN-NOA Technology Development Co., Ltd."
  - Right: "Date of revision: [Date]"
- Font: 9pt (sz=18)

## 12. Footer (repeating on every page)
- Content: page number (auto PAGE field, right-aligned)
- Font: 9pt (sz=18)

## 13. Default Content (when not provided in source)
- Section XIV: "Not classified as dangerous goods."
- Section XV: "Not classified as hazardous chemical according to applicable regulations."
- Section XII: "No data available."

## 14. Content Rules
- Remove any company name that is not SUN-NOA (e.g., OEM manufacturer) entirely
- Do NOT add content not in the source
- Use "Not available" for 无数据
