---
name: research-starter-kit-en
description: English-language methodology handbook for AI/CS research, based on the Research-Starter-Kit by LAMDA-NeSy at Nanjing University. Use for English queries when writing or revising any paper section (Abstract, Introduction, Related Works, Methods, Experiments, References), diagnosing a draft that "reads like a lab report", designing paper figures (teaser, method diagram, results plots) and color schemes, responding to reviewers (rebuttal, AC message), preparing a group meeting or conference talk, planning how to find and read papers, or advising on scholarships and research habits. Delivers "what is wrong + which standard it violates + how to fix it", not paper templates. For Chinese queries use research-starter-kit.
agent_created: true
---

# Research Starter Kit (English)

A library of criteria and revision moves, not templates. When a user brings a draft, first determine which standard it violates, then give a concrete fix.

## 1. Route before answering

| The user wants to | Read |
| --- | --- |
| Pick a topic, find papers, read papers, generate ideas, give a talk, run meetings, build habits | `references/01-research-workflow.md` |
| Write or revise Abstract, Introduction, Related Works, Methods, Experiments, References | `references/02-paper-writing.md` |
| Design a teaser, method figure, or results figure; choose colors; write captions | `references/03-paper-figures.md` |
| Respond to reviewers, write an AC message | `references/04-rebuttal.md` |
| Attend a conference, apply for scholarships, use AI tools, further reading | `references/05-academic-life.md` |

Rules:

- When the question is "how should this section be written" or "how should this figure be drawn", **read the relevant file first**, then answer with the criteria and examples it contains. Do not answer from generic writing advice.
- For compound requests ("tighten my abstract and design a teaser for it"), read both `02` and `03`.
- If the user only wants a one-line answer (e.g., "what chart for a reward curve"), read the file, then answer with the conclusion plus one reason — do not dump the chapter.

## 2. Three principles that run through everything

1. **A paper is a statement of contribution, not a log of work.** A reader must be able to answer three things: what problem is solved, what the key idea is, what the contribution means to the field. Any "we did A, then B" paragraph gets reorganized into a chain of contribution.
2. **Structure before prose.** Every section has a fixed function (abstract = statement of contribution, introduction = funnel, methods = why the design is this way, experiments = evidence for claims). When structure is wrong, do not polish sentences first — align paragraph functions.
3. **The reviewer reads once.** The first three sentences of the abstract and the first glance at Figure 1 must carry the core claim. Ask of every change: could this make a one-pass reader miss the point?

## 3. Section-level criteria (quick reference)

- **Abstract**: five sentences — context (1), scientific problem (1–2, **most critical**), methodological idea (1–2), quantified result (1), plus a closing check that the result answers the stated problem. A problem phrased as an empirical phenomenon ("LLMs often fail in X") lands the paper in borderline territory; lift it to a mechanism (flawed theory, weak generalization, insufficient robustness).
- **Introduction**: four-part funnel — why the field matters → what prior work achieved → what gap remains → what this paper does, how, and with what result. Never open with your own method.
- **Related Works**: organize by category and contrast, set up the gap. No laundry lists; every category must end on the difference from this paper.
- **Methods**: motivation and intuition first, formalism second. Every module answers "why is this needed", not just "what it is". Every formula gets a why-before, a symbol-after, and a role-after.
- **Experiments**: every experiment maps to one claim — main results for SOTA, ablations for necessity of parts, analysis for mechanism. State the comparison settings, not just the numbers.
- **References**: cite only what you have read; one consistent format; no filler citations.

Details, worked examples, and sentence templates are in `references/02-paper-writing.md`.

## 4. Figures

Three kinds, three criteria: **teaser** carries only "problem or observation + this paper's advantage"; **method figure** shows modules and data flow; **results figure** makes the trend visible at a glance.

Before drawing, you must be able to state one sentence: "what should a reader remember from this figure." If you cannot, do not draw it yet.

Hard requirements:

- **Self-Contain**: the figure is understandable without the main text. Expand every abbreviation at first use.
- **One semantic color**: exactly one saturated color marks "wrong / failure / our advantage"; all other color belongs to the content itself. Prefer colorblind-safe palettes (Okabe-Ito, Tableau 10).
- **Double coding**: never let color carry meaning alone; back it with shape or text.
- **Vector export**: prefer SVG / EPS / PDF; after export, shrink to the actual two-column size and re-check type size and line weight. If it is unreadable at that size, it fails.
- **Four-part caption**: `Figure N.` + bold subtitle + one summary sentence + `(left)/(top)/(bottom)` anchors + a statement of the advantage. Reviewers always read captions — proofread them separately.

Case analyses, color tools, and asset libraries are in `references/03-paper-figures.md`.

## 5. Rebuttal

- **Do not drop a point.** Answer every comment; merge similar ones, but never delete one to save space.
- **Read the reviewer's inclination.** Satisfy those who state "fix X and I raise my score"; consolidate positives; spend the most space on negatives; exploit contradictions between reviewers.
- **Strike first on factual errors.** When a reviewer is factually wrong, say so in the first sentence and mirror it to the AC to lower that review's weight.
- **Space is a resource.** Abbreviate aggressively and spend the words where a score can still flip.
- **Structure**: common concerns first, then reviewer by reviewer, ending with committed revisions.
- Calm tone; no emotion; do not restate the review verbatim.

Tactics per scenario (novelty, factual error, marginal gain, insufficient experiments) and English phrasing templates are in `references/04-rebuttal.md`.

## 6. Pre-delivery checks

**Manuscript**: does the abstract stand alone and state the contribution? Does paragraph 1 of the introduction talk about the field rather than your method? Does every experiment map to a claim? Is every claimed contribution backed by evidence?

**Figures**: can you state each figure's purpose in one sentence? Is the text still legible at two-column size? Is any information conveyed by color alone? Does the caption explain what (a)(b)(c) are?

**Rebuttal**: is every comment answered and cross-referenced? Are promised experiments marked "will be provided in the final version"? Is there any emotional phrasing left?

## 7. Boundaries

- Diagnose, restructure, and rewrite for expression only. **Do not invent research contributions, fabricate experimental numbers, or fabricate references.** Citations must be verifiable; when unsure, mark them "to be verified".
- When the user has a Chinese draft but targets an English venue, fix the logical skeleton first, then the English — do not translate sentence by sentence.
- The content derives from the public materials of the original author (Guo Lanzhe et al., Nanjing University). For field-specific conventions, remind the user to follow the latest requirements of that venue.

## 8. Reference files

| File | Contents |
| --- | --- |
| `references/01-research-workflow.md` | Chapters 01–07: what research is, finding papers, reading papers, generating ideas, academic talks, efficient meetings, good habits |
| `references/02-paper-writing.md` | Chapters 08, 10–15: writing overview and Abstract / Introduction / Related Works / Methods / Experiments / References |
| `references/03-paper-figures.md` | Chapter 09: teaser, method figure, results figures, real-paper case analyses, color audits, tools |
| `references/04-rebuttal.md` | Chapter 16: rebuttal principles, scenario handling, AC messages, English phrasing |
| `references/05-academic-life.md` | Chapters 17–19 and appendix: conferences, scholarships, AI tools, further reading |

For long files, search by keyword, for example:

```bash
grep -n "five-sentence\|four-part\|teaser\|Self-Contain\|AC message" references/*.md
```
