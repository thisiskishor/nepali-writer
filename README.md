# Nepali Writer Skill for Claude Code

**Original Author:** Kishor Gartaula ([@thisiskishor](https://github.com/thisiskishor))  
**License:** MIT — Use freely, modify, and share with attribution (see [LICENSE](LICENSE) and [NOTICE.md](NOTICE.md) for details)

---

## What's Included

A Claude Code skill that writes, translates, and refines Nepali text at native, educated standard.

**Handles:**
- ✅ English → Nepali translation (formal, informal, technical, marketing)
- ✅ Nepali → English translation with cultural nuance
- ✅ Formal business letters, official documents, proposals
- ✅ Social media content and conversational writing
- ✅ Technical documentation and domain-specific writing
- ✅ Grammar, orthography, honorifics, punctuation correction
- ✅ Localization for Nepali-speaking audiences
- ✅ Literary and poetic Nepali writing

**Standards:** Nepal Academy orthography rules, modern Nepali conventions, cultural appropriateness.

---

## ⚠️ Status & Ongoing Development

**Nepali Writer is functional but still evolving.** While the skill provides comprehensive guidance on Nepali grammar, orthography, and translation based on Nepal Academy standards, **edge cases and complex linguistic nuances may occasionally be missed.** The skill improves with usage and feedback.

**Current strengths:**
- Core grammar and honorific system
- Orthography and script rules
- Common mistake patterns and corrections
- Translation protocols
- Domain-specific guidance

**Areas being expanded:**
- More real-world examples across all domains
- Regional dialect support
- Additional technical/specialized terminology
- Literary and poetic forms

**Your contributions help!** If you find errors, have better examples, or want to expand coverage, please contribute via the [Contributing Guidelines](CONTRIBUTING.md). Together we make Nepali language AI assistance world-class.

---

## Quick Start

### Installation

**Option A — Download as ZIP (easiest)**

1. Click the green **Code** button at the top
2. Click **Download ZIP**
3. Extract the ZIP
4. Copy the `nepali-writer` folder into your Claude skills directory:

**Mac/Linux:**
```bash
cp -r nepali-writer ~/.claude/skills/skills/engineering/
```

**Windows (PowerShell):**
```powershell
Copy-Item -Recurse nepali-writer "$env:USERPROFILE\.claude\skills\skills\engineering\"
```

If the `engineering` folder doesn't exist:
```bash
mkdir -p ~/.claude/skills/skills/engineering
```

### Option B — Clone the repo

```bash
git clone https://github.com/thisiskishor/nepali-writer.git
cp -r nepali-writer ~/.claude/skills/skills/engineering/
```

The skill loads automatically — no restart needed.

---

## How to Use

Once installed, invoke nepali-writer with natural language or slash commands:

### Direct Commands
```
/nepali-writer translate "Write this formal letter in Nepali"
/nepali-writer write "A professional email to a government office"
/nepali-writer refine "Check this Nepali text for errors"
```

### Trigger Phrases (activate automatically)
- "write it in Nepali" / "लेख्नुहोस्"
- "translate this to Nepali"
- "translate this to English" (when source is Nepali)
- "fix the grammar" / "correct this"
- "make it more formal" / "make it conversational"
- Any Nepali Devanagari text for translation/editing/correction

### Examples

**English → Nepali (Formal Letter)**
```
User: "Write a formal request letter in Nepali asking for a deadline extension"

Output:
आदरणीय श्रीमान् शर्माजी,

उपर्युक्त विषयमा यस कार्यालयमा निवेदन दिनु परेकाले सादर निवेदन गर्दछु कि 
प्रकल्प प्रस्तुत गर्ने समयसीमा अलिकति बढाइपाऊँ भनी विनती गर्दैछु...
```

**Informal Social Media**
```
User: "Translate this to Nepali for Instagram: Just launched our new coffee shop!"

Output:
काठमाडौँमा हाम्रो नयाँ कफी शप खुलियो! ☕ आउनुहोस् र खान आनन्द गर्नुहोस्
```

**Grammar Correction**
```
User: "Fix this: दिदि यहाँ बस् ।"

Output:
✓ दिदी यहाँ बस्नुहोस् । (formal pronoun with formal verb)
  OR
✓ तिमी यहाँ बस । (informal pronoun with informal verb)

Explanation: Verb form must match pronoun honorific level
```

---

## What You Get

### Core Skill (`nepali-writer/SKILL.md`)

Complete guidance covering:

**Foundations:**
- Devanagari script and Nepali phonetics
- SOV (Subject-Object-Verb) sentence structure
- Three-level honorific system (critical for Nepali)
- Verb conjugation (present, past, future, imperative)
- Raswa/Dirgha (vowel length rules)
- Postpositions and case markers
- Punctuation with danda (।)

**Usage Guides:**
- Formal letters and official documents
- Email writing conventions
- Social media and conversational content
- Technical documentation
- Business communication
- Literary/poetic Nepali
- Domain-specific terminology

**Common Mistakes:**
- Wrong sentence structure (SVO vs SOV)
- Honorific mismatches
- Split honorific compounds (Padyog errors)
- Raswa/Dirgha spelling mistakes
- Postposition spacing issues
- Literal English idiom translation
- Latin period instead of danda

**Translation Protocol:**
- Step-by-step English → Nepali translation
- Step-by-step Nepali → English translation
- Register matching and tone preservation
- Cultural context handling
- Idiom adaptation

### References

**examples/** folder includes:
- Formal letter samples (English + Nepali)
- Business email templates
- Social media content (multiple tones)
- Technical documentation examples
- Translation comparison examples

---

## Skill Structure

```
nepali-writer/
├── SKILL.md                       - Complete skill definition
└── references/
    └── domain-wisdom.md           - Nepal Academy standards & best practices
```

---

## Integration with Other Skills

Nepali-writer pairs powerfully with:

- **content-writing** → English content → Nepali translation
- **email-writing** → English email structure → Nepali with correct honorifics
- **copywriting-classic** → English marketing → Nepali localization
- **code-recon** → Understand systems → Document in Nepali

**Workflow Example:**
```
1. Use content-writing to structure English blog post
2. Apply nepali-writer to translate/adapt to Nepali
3. Result: Culturally appropriate, well-written Nepali content
```

---

## Key Features

✅ **Nepal Academy Standards** — All orthography follows official Nepali guidelines  
✅ **Honorific System** — Correctly handles all three formality levels (तँ, तिमी, तपाईं)  
✅ **SOV Structure** — Automatically applies subject-object-verb order  
✅ **Raswa/Dirgha** — Accurate vowel length distinction (most common AI mistake)  
✅ **Padyog** — Honorific compound verbs written as one word  
✅ **Danda Punctuation** — Uses । instead of Latin period  
✅ **Cultural Context** — Understands Nepali festivals, titles, respectful address  
✅ **Domain-Specific** — Technical, legal, academic, marketing, literary  
✅ **Verification Checklist** — Pre-output quality assurance step-by-step  
✅ **Worked Examples** — Real translation and writing examples  

---

## Who Benefits

- **Content creators & marketers** targeting Nepal or Nepali diaspora
- **Organizations** translating products/services to Nepali
- **Nepali writers** seeking to polish their work professionally
- **Localization teams** handling Nepali language requirements
- **Educators & academics** writing in Nepali
- **Developers** documenting software in Nepali

---

## Standards & References

This skill is based on:

1. **Nepal Academy (प्रज्ञा-प्रतिष्ठान)** — Official language authority
2. **Nepali Brihat Shabdakosh** (नेपाली वृहत् शब्दकोश) — Definitive dictionary
3. **Modern Nepali conventions** — Post-2015 Constitution standards
4. **Cultural context** — Nepali social norms, festivals, respectful address
5. **Industry best practices** — Localization, technical writing, marketing

---

## License & Attribution

This skill is licensed under the MIT License with an **attribution requirement**.

**If you modify and republish this skill, you must:**
- Retain the copyright notice: "Copyright (c) 2026 Kishor Gartaula"
- Credit the original author and link to https://github.com/thisiskishor
- Clearly indicate what you modified
- Include the LICENSE file with your distribution

See [NOTICE.md](NOTICE.md) for full details.

**Original author:** [Kishor Gartaula](https://github.com/thisiskishor) — [kishorgartaula.com.np](https://www.kishorgartaula.com.np)

---

## Examples

See [`examples/`](examples/) for:
- Formal letter samples (before/after)
- Translation examples (English ↔ Nepali)
- Social media content (multiple registers)
- Technical documentation examples
- Grammar correction walkthroughs

---

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Worth contributing:**
- Better examples or corrections from your experience
- New domain-specific examples (legal, medical, academic)
- Improvements to translation protocol
- Nepal Academy updates or corrections
- Real-world translation samples

Your feedback and contributions make this skill better for everyone.

---

## Support This Work

If you find Nepali Writer valuable, consider supporting the creator:

<div>
  <a href="https://ko-fi.com/thisiskishor" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/Ko--fi-FF5E8A?style=flat-square&logo=ko-fi&logoColor=white&label=Buy%20me%20a%20coffee" alt="Ko-fi">
  </a>
  <a href="https://www.kishorgartaula.com.np/buy-coffee" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/ESewa%20%7C%20Khalti-FF6B35?style=flat-square&logo=wallet&logoColor=white&label=Local%20Payment" alt="Local Payment">
  </a>
</div>

---

## Related Projects

- **[code-brain](https://github.com/thisiskishor/code-brain)** — Persistent memory skill for project sessions
- **[code-recon](https://github.com/thisiskishor/code-recon)** — Codebase topology mapping before touching code

---

**Made with ❤️ for the Nepali language and community**
