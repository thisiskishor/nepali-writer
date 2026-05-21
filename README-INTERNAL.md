# Nepali Writer Skill — Internal Context Guide

**For Claude agents and developers working with this skill.** Comprehensive reference for understanding skill structure, usage, limitations, and contribution workflows.

---

## Skill Purpose & Scope

### What This Skill Does

`nepali-writer` is a Claude Code skill that enables writing, translating, and refining Nepali text at native, educated standard across formal, semi-formal, and informal registers.

**Core capabilities:**
- English → Nepali translation (preserving tone, register, cultural context)
- Nepali → English translation with cultural nuance
- Formal business letters, official documents, proposals
- Social media and conversational content
- Technical documentation with domain-specific terminology
- Grammar, orthography, honorifics, punctuation correction
- Localization for Nepali-speaking audiences
- Literary and poetic Nepali writing

### What This Skill Does NOT Do

- Provide character-by-character spell checking (use dedicated spell checkers)
- Generate Nepali content from scratch without reference/context
- Replace professional human translators for critical documents
- Handle all regional dialects (focuses on standard modern Nepali)
- Provide legal or medical advice (can format documents, but not specialize)
- Automate large-scale batch translation without quality review

---

## Skill Architecture & File Organization

### Folder Structure

```
nepali-writer/
├── README.md                      (Public GitHub version — simplified)
├── README-INTERNAL.md             (This file — detailed for agents)
├── LICENSE                        (MIT license with copyright notice)
├── NOTICE.md                      (Attribution requirements)
├── CONTRIBUTING.md                (Contribution guidelines + known issues)
├── CHANGELOG.md                   (Version history and roadmap)
└── nepali-writer/
    ├── SKILL.md                   (Main skill definition — 10,000+ words)
    ├── examples/
    │   ├── examples-index.md      (Index of all examples with links)
    │   ├── example-1-formal-letter.md
    │   ├── example-2-social-media.md
    │   ├── example-3-technical-docs.md
    │   ├── example-4-grammar-corrections.md
    │   ├── example-5-translation-comparison.md
    │   └── example-6-register-variations.md
    └── references/
        └── domain-wisdom.md       (20 core wisdoms + best practices)
```

### How Files Connect

```
┌─────────────────────────────────────────────┐
│  User Request (translate, write, refine)    │
└──────────────────┬──────────────────────────┘
                   │
                   ▼
        ┌──────────────────────┐
        │   SKILL.md (main)    │◄─── Foundational knowledge
        │  10,000+ words       │     (grammar, SOV, honorics, etc)
        └──────────────────────┘
         │         │         │
         ▼         ▼         ▼
    ┌────────┐ ┌────────┐ ┌────────────┐
    │Examples│ │References│ │Verification│
    │        │ │          │ │ Checklist  │
    └────────┘ └────────┘ └────────────┘
       │          │              │
       │          │              │
  Real-world   Core 20      Quality gate
  patterns    Wisdoms        before output
```

### How to Use Each File

| File | Purpose | When to Reference | How Agents Use It |
|------|---------|-------------------|-------------------|
| **SKILL.md** | Complete guidance on all aspects | Always; for comprehensive understanding | Read full SKILL.md context for request type |
| **examples-index.md** | Overview of all 6 examples | Finding right example for context | Use for pattern matching |
| **example-1 through 6** | Real-world application patterns | Specific domain or register needed | Analyze patterns relevant to user request |
| **domain-wisdom.md** | 20 core principles + reference table | Quick lookup; verification checklist | Use for error correction, verification |
| **CONTRIBUTING.md** | Known issues & contribution process | When refining or acknowledging limitations | Understand what's incomplete/improving |

---

## How Agents Should Use This Skill

### For Translation Requests

1. **Read SKILL.md "Translation Protocol" section** — Understand the step-by-step process
2. **Check relevant example** — E.g., Example 1 for formal letters, Example 5 for idioms
3. **Apply domain-wisdom** — Especially wisdoms #3 (dative), #11 (literal translation fails)
4. **Use verification checklist** — From SKILL.md or domain-wisdom.md
5. **State limitations if applicable** — "This translation assumes modern standard Nepali, not regional dialects"

### For Writing Requests

1. **Identify register** — Formal, semi-formal, or informal (check Example 6)
2. **Read SKILL.md "Domain-Specific Writing Guides"** — For the domain (letter, email, technical, etc)
3. **Reference relevant example** — E.g., Example 1 for letters, Example 2 for marketing
4. **Apply tone & register guide** — From SKILL.md
5. **Verify against checklist** — Ensure honorific matching, SOV order, danda punctuation

### For Grammar/Correction Requests

1. **Use Example 4: Grammar Corrections** — Common patterns and fixes
2. **Reference domain-wisdom wisdoms #4-6, #11-14** — Core mistake patterns
3. **Run through verification checklist** — From SKILL.md "Pre-Output Verification"
4. **Explain the rule** — Help user understand *why* the correction was made

### For Uncertain Requests

**If you're unsure:** Acknowledge the limitation and reference Nepal Academy standards as authority.

**Examples:**
- "Nepal Academy standards prefer [term] over [term], which I've used. [Alternative term] is also acceptable."
- "This translation follows modern standard Nepali. Regional variants may differ."
- "I'm uncertain about this term. Nepal Academy defines it as [definition]."

---

## Key Limitations & Known Issues

### Known Items for Review

These translations in the examples are flagged for potential refinement:

1. **Example 1, Line 3:** "आमाद टोलीलाई" 
   - Current: "आमाद टोलीलाई" (our team)
   - Issue: Verify if "आमाद" is correct or should be "हाम्रो"
   - Status: ✓ CORRECTED to "हाम्रो टोलीलाई"

2. **Example 3, Technical Terminology:** "डिस्क स्पेस" vs "डिस्क स्थान"
   - Current: Explained both; "डिस्क स्थान" recommended for formal
   - Issue: No single standard; industry usage varies
   - Status: ⚠️ Noted as acceptable variation; guidance provided

3. **Example 5, Idiom Translation:** "खुसी" vs "खुशी" (happy)
   - Current: "खुशी लाग्यो" (Raswa/Dirgha corrected)
   - Issue: Long ी (dirgha) is correct for "happy"
   - Status: ✓ CORRECTED to "खुशी"

### General Limitations

1. **Regional Dialects Not Covered**
   - Skill focuses on standard modern Nepali
   - Newari, Maithili, Bhojpuri dialects not yet included (future Phase 2)

2. **Classical/Old Nepali Not Covered**
   - Focuses on post-2015 Constitution standards
   - Ancient literary Nepali (Motiram Bhatta era) not detailed

3. **Speed Limitations for Large-Scale Batch Work**
   - Skill works best for individual documents/sections
   - Large-scale translation projects may need human review

4. **Edge Cases & Linguistic Nuance**
   - Complex metaphors, cultural idioms may occasionally be missed
   - Antarctica-specific vocabulary, niche technical terms require context

5. **Real-Time Language Evolution**
   - New vocabulary (tech, social media) emerges constantly
   - Skill updates based on Nepal Academy changes and community feedback

### How to Report Issues

See [CONTRIBUTING.md - Known Items for Review](CONTRIBUTING.md#known-items-for-review) for process to submit corrections.

---

## Integration Points with Other Skills

### Recommended Skill Pairings

1. **With content-writing skill:**
   - Create English blog post → Translate to Nepali
   - Workflow: content-writing (structure) → nepali-writer (translation)

2. **With email-writing skill:**
   - Draft English email → Translate and match Nepali register/tone
   - Workflow: email-writing (structure) → nepali-writer (localization)

3. **With copywriting skill:**
   - Create English marketing copy → Localize to Nepali with cultural nuance
   - Workflow: copywriting (messaging) → nepali-writer (culturalization)

4. **With code-recon skill:**
   - Audit codebase → Document findings in Nepali
   - Workflow: code-recon (findings) → nepali-writer (Nepali documentation)

---

## Verification & Quality Assurance

### Pre-Output Verification Checklist

**Before returning Nepali text to user:**

- [ ] **Structure:** SOV word order correct, adjectives placed correctly, postpositions attached
- [ ] **Honorifics:** Pronoun-verb pairs match in formality level (तपाईं + गर्नुहोस्, not तिमी + गर्नुहोस्)
- [ ] **Orthography:** Raswa/Dirgha vowel lengths correct, Padyog compounds written as one word
- [ ] **Register:** Tone and vocabulary match the context (formal letter, social media, technical, etc)
- [ ] **Punctuation:** Using Devanagari danda (।) not Latin period (.)
- [ ] **Vocabulary:** Domain-appropriate terms used consistently (e.g., अपडेट not inconsistent switching)
- [ ] **Idioms:** Not literal translations; sound natural to native speakers
- [ ] **Cultural Context:** Culturally appropriate forms of address, greetings, closings

**If any box fails:** Note the issue, state what's uncertain, or ask for clarification.

---

## Workflow Examples

### Example: Business Email Translation

```
User Request: "Translate this business email to Nepali"

Agent Workflow:
1. Read SKILL.md "Domain-Specific Writing: Email" section
2. Check Example 1 (formal letter) for register and structure patterns
3. Check domain-wisdom #2 (honorific system) for तपाईं + गर्नुहोस् forms
4. Translate with focus on formal tone
5. Run verification checklist:
   ✓ SOV order maintained
   ✓ तपाईं + गर्नुहोस् consistent (formal)
   ✓ Postpositions attached (घरमा not घर मा)
   ✓ Danda (।) used correctly
   ✓ Vocabulary formal and consistent
6. Deliver with brief note: "Translated using formal register per business email context"
```

### Example: Social Media Copy

```
User Request: "How would this Instagram post look in Nepali?"

Agent Workflow:
1. Read SKILL.md "Domain-Specific Writing: Social Media" section
2. Check Example 2 (social media) for tone and code-mixing patterns
3. Check domain-wisdom #15 (register selection) — informal is appropriate
4. Translate with focus on engagement and tone preservation
5. Run verification checklist:
   ✓ SOV order maintained
   ✓ Informal pronoun/verb forms appropriate (तिमी/गर्)
   ✓ Postpositions correct (घरमा)
   ✓ Danda used correctly
   ✓ Code-mixing acceptable (कफी, पेस्ट्री)
6. Deliver with brief note: "Translated using informal/conversational register per social media context"
```

### Example: Grammar Error Correction

```
User Request: "Fix this Nepali sentence: दिदि यहाँ बस् ।"

Agent Workflow:
1. Check Example 4: Grammar Corrections — Error 1 is exactly this
2. Identify error: Incomplete/mismatched honorific
3. Reference domain-wisdom #2: Pronoun-verb must match
4. Provide both options:
   ✓ Formal: दिदी यहाँ बस्नुहोस्
   ✓ Informal: दिदि यहाँ बस
5. Explain: "The original mixes informal pronoun (दिदि) with incomplete verb (बस्). 
   Choose based on context: formal (दिदी + बस्नुहोस्) or informal (दिदि + बस)"
```

---

## Contribution Workflow

### How to Improve This Skill

See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines. Quick workflow:

1. **Identify issue or improvement**
   - Better example for a domain?
   - Error in translation?
   - Missing terminology?

2. **Submit via GitHub PR with:**
   - Clear description of change
   - Before/after examples
   - Reference to Nepal Academy or other authority
   - Attribution to yourself (will be credited)

3. **Skill maintainer reviews:**
   - Checks against Nepal Academy standards
   - Integrates into relevant files
   - Credits contributor in CHANGELOG

---

## For Future Phases

### Phase 2: Expanded Nepali Scope
- Regional dialects (Newari, Maithili, Bhojpuri)
- Classical/literary Nepali
- Legal document templates
- Academic writing conventions
- Journalistic style guide

### Phase 3: Multi-Language Support
- Nepali ↔ Hindi translation
- Nepali ↔ Maithili translation
- Nepali ↔ Newari translation
- Multi-language terminology glossary

### Phase 4: Tools & Automation
- Raswa/Dirgha spelling checker
- SOV structure validator
- Honorific consistency checker
- Padyog suggestion tool
- Nepal Academy compliance checker

### Phase 5: Integration
- Chrome extension
- VS Code plugin
- API endpoint
- Organization-specific style guides

---

## Quick Reference for Agents

### Most Important Files

1. **SKILL.md** — 10,000+ words of complete guidance
2. **domain-wisdom.md** — 20 core principles (quick lookup)
3. **examples/** — 6 real-world patterns (matching context)

### Most Common Issues

1. **Literal translation** → Use domain-wisdom #11; check Example 5
2. **Honorific mismatch** → Use domain-wisdom #2; check Example 4
3. **Register confusion** → Use domain-wisdom #15; check Example 6
4. **Postposition spacing** → Use domain-wisdom #4; check Example 4

### Most Used Verification Points

1. SOV word order ✓
2. Honorific matching (pronoun + verb) ✓
3. Danda punctuation (।) not period (.) ✓
4. Postposition attachment (no spaces) ✓
5. Raswa/Dirgha correctness ✓

---

## Questions & Context for Agents

**"I'm not sure if this translation is correct..."**
- Reference Nepal Academy standards
- Check relevant example file
- Acknowledge uncertainty: "Nepal Academy defines this term as..."
- Offer alternatives if valid

**"Should I use formal or informal register?"**
- Check Example 6: Register Variations
- Use domain-wisdom #15: Register = Relationship + Context
- Ask user if unclear: "To match the register, could you clarify the relationship and context?"

**"I found an error in the examples..."**
- Check CONTRIBUTING.md - Known Items for Review
- It might be a known issue being refined
- If not listed, report via GitHub PR with explanation

---

## Credits & License

**Author:** Kishor Gartaula (@thisiskishor)  
**License:** MIT (with attribution requirement — see LICENSE and NOTICE.md)  
**Standards:** Nepal Academy (प्रज्ञा-प्रतिष्ठान)  
**Based on:** Nepal Academy standards, Nepali Brihat Shabdakosh, modern Nepali conventions

---

**This guide is for Claude agents and developers using the nepali-writer skill. For user-facing documentation, see README.md.**
