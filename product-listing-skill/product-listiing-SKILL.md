---
name: Product Listing Generator
description: Generates ready-to-paste B2B product listings (title, description, features, specs) in a consistent professional format for platforms like TradeWheel, Made-in-China, Alibaba, and our own website.
---

# Product Listing Generator

## Purpose
Generate standardized, professional B2B product listings from a product's basic information, matching SUN-NOA's company tone (concise, descriptive, professional, not salesy).

## Input Required from User
Ask the user (or use available data) for these fields:
1. Product name / model number
2. Product category (EPI, PVAc, EVA Hot Melt, PUR, MS Polymer, Silicone, Epoxy, etc.)
3. Key features (bond strength, water resistance, curing, open time, etc.)
4. Specifications (viscosity, solids content, pH, specific gravity, application temp, etc.)
5. Applications / end-use
6. Packaging
7. Certifications (D4, JAS, EAC, REACH, SGS, etc.)
8. MOQ, price (if provided)
9. Target platform (TradeWheel, Made-in-China, Alibaba, website)

## Output Format (Always follow this structure)

### 1. Product Title (1 line, keyword-rich, max ~15 words)
Example: "Two-Component EPI Wood Adhesive – D4 Compliant, Formaldehyde-Free, for Solid Wood Edge/Face Gluing"

### 2. Product Overview (2-3 sentences, what it is + main benefit)

### 3. Key Features (bullet points, 5-8 items, start with action/benefit words)

### 4. Applications (bullet points, concise)

### 5. Specifications Table (model | spec | description)

### 6. Certifications (line)

### 7. Packaging (line)

### 8. Additional Fields (MOQ, Price, Port, Payment, HS Code)

## Style Rules
- Concise, descriptive, professional tone.
- No exaggerated marketing language ("amazing", "incredible", "best").
- Use accurate industry terminology.
- Consistent spelling: use "optimization" (US) unless told otherwise.
- Clear, scannable formatting.
- Highlight certifications.

## Note
If any required information is missing, insert [bracketed placeholders] so the user can fill them in.
