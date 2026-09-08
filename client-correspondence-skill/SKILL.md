---
name: client-correspondence
description: Drafts and polishes bilingual (Chinese–English) business correspondence — WeChat / group-chat messages and emails to clients, customers, partners and suppliers — applying the SUN-NOA professional register (indirect, passive-leaning tone) with anti-AI-sounding guardrails. Use when the user asks to draft, rewrite, or polish a reply or message to a client, partner, supplier, or business contact in Chinese and/or English.
---

# Client Correspondence (Bilingual CN–EN)

## Purpose
Produce professional, natural-sounding business messages in Chinese (CN), English (EN), or both, for the user's client-facing work. The skill supplies the tone — the user does not need to provide a "personal style". English output follows two defined registers (formal vs. casual-formal); Chinese output draws on an authentic business-formula library (see glossary.md) so it never reads like a machine translation from English.

## When to Use
Use whenever the user asks to:
- draft a reply / message / email to a client, customer, partner, supplier, or new contact
- polish or rewrite an existing draft so it "sounds more professional" or "less AI-generated"
- prepare a group-chat (GC) message, including cases where bosses/decision-makers are in the group
- write a message in Chinese that must read like natural Chinese business writing

Do NOT use for: technical document translation (use tds-translator / msds-translator), meeting kits or minutes (use meeting materials templates when available).

## Required Inputs (ask if not provided)
1. **Recipient & relationship** — name (e.g., 稻垣先生 / Mr. Inagaki), company, new or established contact
2. **Channel** — WeChat message, group chat, or email
3. **Language(s)** — CN, EN, or both. Default: mirror the client's latest language; if unsure whether the reader reads Chinese (e.g., a Japanese contact who may not), include EN
4. **Formality level** — Formal (default) or casual-formal; see Tone Levels below
5. **Content/intent** — what must be said (confirm, thank, request, welcome, decline, follow up…)
6. **Approved facts only** — see Decision Gates below

## Tone Levels
- **Formal (F)** — default. Clients, first contacts, anything involving pricing/terms/negotiation, and any group chat where decision-makers of either side are present.
- **Casual-formal (C)** — established contacts, logistics, quick confirmations, warm follow-ups. Lighter but still polite.
When in doubt use F. If the user says "make it less formal / more natural / shorter", move toward C.
Full register rules: see **tone-guide.md**.

## Workflow
1. Collect the Required Inputs (ask only for what is missing — never guess recipient or facts).
2. If the user provides sample messages whose tone they want to mimic (their own, a colleague's, or a client's), extract the recurring patterns — openings, closings, sentence rhythm, degree of directness — and apply them.
3. Decide intent(s), and separate:
   - **facts** (dates, names, already-agreed items) → include as stated
   - **commitments/decisions** (prices, terms, promises, accepting proposals) → see Decision Gates
4. Draft in the required language(s):
   - EN: apply tone-guide.md register rules for the chosen level.
   - CN: build from glossary.md formulas; keep sentences short; mirror the client's numbering when replying to a numbered message; never translate English idioms literally.
   - Both languages: CN line then EN line (or EN line then CN line, whichever the user prefers — ask if unclear). Group-chat messages: keep each language block together so the reader can follow.
5. Run the Self-Check (below) and fix anything flagged.
6. Output **plain text**, copy-paste ready. If the user requests a file, produce a .docx using the message content only (no special header).

## Decision Gates (important)
- **Never invent** prices, dates, quantities, claims, product facts, or the client's obligations.
- If the message would **commit the company** (confirm an agreement, accept a proposal, promise delivery, state pricing): ask the user whether leadership has approved it.
  - If approved → state it plainly.
  - If NOT approved → either draft a neutral receipt-only version, or phrase it as pending confirmation, e.g. CN: "我方确认后会尽快回复" / EN: "we will reply shortly once confirmed internally."
- If the user is a junior member and bosses are in the group chat, do NOT write as if the user decides company policy. Attribute decisions to the company/leadership: "我方领导确认后…", "关于…由我方领导直接回复更合适".
- Flag anything that looks like it should be handled 1-on-1 rather than in the group chat (e.g., price negotiation), and suggest taking it offline.

## Self-Check (always run before output)
- **AI-sound check:** no bullet lists inside short WeChat messages; no template-y openings; no over-hedging ("I think it might possibly be…"); varied sentence rhythm; reads like a person typed it.
- **Tone check:** passive/indirect for arrangements and requests; active for warmth. Not everything passive.
- **CN naturalness check:** every CN sentence should be something a native business writer would actually type; if a phrase came from direct EN translation, replace it with the glossary formula.
- **Fact check:** only approved facts; no placeholder prices.
- **Register check:** matches the chosen level (F vs C) consistently.

## Skill Files
- `tone-guide.md` — full register rules: EN formal patterns, EN casual-formal patterns, CN formula guidance, anti-AI checklist, annotated before/after examples
- `glossary.md` — CN⇄EN phrase library by intent + business vocabulary (SUN-NOA / woodworking adhesive context)
- `templates/message-templates.md` — ready skeletons (WeChat warm, formal numbered confirmation, GC welcome, internal note to boss, formal email, polite deferral)
