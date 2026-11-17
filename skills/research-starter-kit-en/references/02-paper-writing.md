This file covers the whole writing chain: overall strategy, plus how to write the Abstract, Introduction, Related Works, Methods, Experiments, and References — with common mistakes for each.

## 08 · How to Write a Paper (Overview)

### Before you start

- **Settle authorship**: order by contribution. The first author writes the paper; the corresponding author owns the research.
- **Settle the target venue**: choose a venue that matches the strength of the work — usually decided by the advisor.

### What a paper actually says

- Problem X is important
- Previous works A, B, and C have been done
- A, B, and C have their weaknesses
- Your Work D
- Why D is better
- Experimental comparison against A, B, and C
- Strength and Weakness of D
- Future work on D

### The outline

A scientific paper has a clear structure: Title → Abstract → Introduction → Related Works → Your Contribution (Method, Observation, Benchmark, Analysis, etc.) → Support (theoretical or experimental) → Conclusion.

> Figure 8-1　The standard paper structure (schematic, drawn from the original "paper outline"). Key points: Title / Abstract (a statement of contribution, five sentences) / Introduction (field → prior work → open problem → this paper) / Related Works (categorize and compare, set up the gap) / Your Contribution (Method / Observation / Benchmark / Analysis) / Support (proof or experiments) / Conclusion

---

## 10 · How to Write the Abstract

### 10.1　The basic idea

An abstract is not a "summary of the paper" but a **statement of contribution**. Its job is not to cover everything but, within a short space, to make the reviewer understand clearly: what problem this paper solves, what the key idea is, and why the contribution matters to the field. So it should not be long — it should be dense and logically tight.

### 10.2　The five-sentence principle

In general, an abstract can follow the "five-sentence principle", covering five core elements:

> Figure 10-1　How the five-sentence principle allocates elements in an abstract (schematic, from the original). Key points: task context | 1 sentence: broad direction + task scope, no general-knowledge warm-up / 1–2 sentences: the challenge must be *structural* / scientific problem / "LLMs often fail in xxx" is an empirical phenomenon → lands you in borderline territory; push it up to the mechanism / the most critical part / methodological novelty | 1–2 sentences: distill the idea, explain *why it logically solves the problem* / conclusion and contribution | 1 sentence: quantifiable (how many datasets, compared against whom, how much gain) / closing check: the experimental conclusion must answer the scientific question raised earlier (if you claim weak robustness, prove robustness with experiments)

1. **Task context — 1 sentence.** Describe the broad direction and task scope in the most compact language, so the reviewer can immediately place the paper's area and core question. No general-knowledge warm-up; go straight to the point.
2. **Scientific problem — 1–2 sentences (the most critical part).** This matters more than the method. State the challenge and pain point of existing work. Ideally it is a **structural problem**, not an **empirical phenomenon** — or a structural problem distilled from an empirical phenomenon. "LLMs often fail in xxxx task" is an empirical phenomenon: it reads as patching and as a minor contribution, and lands the paper in borderline territory at once. Give the more essential problem, lifting the phenomenon to a mechanism — is the theory flawed, is generalization weak, is robustness insufficient?
3. **Methodological novelty — 1–2 sentences.** Propose the core solution and distill the idea; do not pile on details. To fix weak robustness, what is the approach — a new architecture, a new loss, a new data-synthesis method? What is the core idea? The key is to make the reviewer understand **why this approach logically solves the problem above**.
4. **Conclusion and contribution — 1 sentence.** Describe experiments with concrete, quantifiable metrics rather than generalities. Many students write "significant performance improvement", which is unremarkable because any paper can claim it. Say instead on how many datasets, against which representative methods, on which metric, you improved by how much. One more point, important and often missed: **the experimental conclusion must answer the scientific question raised earlier, forming a logical loop** — if the paper claims to fix insufficient robustness, the experiments should highlight how much more robust the method is under which perturbations or variations, compared with existing methods; reporting overall accuracy alone usually does not support the core claim.

### 10.3　Good examples

The three examples below are all from ICML 2025 and correspond to the three most common abstract patterns: problem-driven, constraint-solving, and benchmark.

#### Example 1 · Propose an algorithm from problem analysis

ICML 2025 Outstanding Paper: *Train for the Worst, Plan for the Best: Understanding Token Ordering in Masked Diffusions*

This paper starts from problem analysis and derives an algorithm. The problem statement is sharp and essential: "trade off complexity at training time with flexibility at inference time"; the conclusion is highly persuasive: **from 7% to 90%**, beating a model with 7× the parameters.

#### Example 2 · Solve one concrete constraint of existing methods

ICML 2025 Oral: *Accelerating LLM Inference with Lossless Speculative Decoding Algorithms for Heterogeneous Vocabularies*

The very common type — "solve problem X of existing method Y" — which resembles what most students do. One sentence for context: accelerating LLM inference matters. Two sentences for the problem: speculative decoding methods require the drafter and target models to share the same vocabulary. One sentence for the work: a method that does not depend on the shared-vocabulary constraint. The experiments answer the acceleration problem: **2.8× speedup** without the constraint.

#### Example 3 · Benchmark or dataset paper

ICML 2025 Oral: *LLM-SRBench: A New Benchmark for Scientific Equation Discovery with Large Language Models*

One sentence for context: scientific equation discovery matters. Two sentences for context and problem: LLMs have drawn much attention for symbolic regression, but evaluation is hard and does not reflect true capability. This paper proposes LLM-SRBench, covering 239 problems across 4 domains and 2 categories (LLM-Transform and LSR-Synth). Then state how many models were evaluated — replacing "several SOTA methods" with "how many classes of algorithms and how many models" would be better. The conclusion states what phenomenon was found and what it contributes to the field.

---

## 11 · How to Write the Introduction

> **Tip**　Once the abstract is done, the Introduction is essentially its expanded version, following the same logic:
>
> field → prior work → open problem → this paper
> A good Introduction usually does four things:
> - explain why the field matters
> - summarize what prior work has done
> - point out what remains unsolved, missing, or insufficient
> - state what this paper does, how, and with what results

### 11.1　The four-part funnel

> Figure 11-1　The four-part funnel of an Introduction (schematic, from the original "four-part structure"). Key points: ① the field: why it matters (scientific / engineering / industrial value) / ② prior work: how far others got (categories + representative work) / ③ open problem: the remaining gap / ④ this paper: what was done, how, and with what result

#### 1. Establish the field

The first part answers: why does this area deserve attention?

You can write about:

- the importance of the problem in science, engineering, medicine, society, or industry;
- why the direction has drawn attention in recent years;
- the application scenarios or theoretical significance of the task;
- brief definitions of the basic concepts, objects, or phenomena.

Note: do not start with your own method. First make the reader understand why the problem matters.

Useful sentence patterns:

```
X is important because ...
X has received increasing attention due to ...
X plays a central role in ...
Recent advances in Y have made it possible to ...
```

#### 2. Review prior work

The second part answers: what have others already done?

This is not a full literature review. Select the work most relevant to this paper and set up the gap.

You can write about:

- the main categories of existing methods;
- which problems the representative work solved;
- what progress that work brought;
- what the current mainstream paradigm is.

Useful sentence patterns:

```
Previous studies have investigated ...
Several methods have been proposed to ...
Existing approaches typically rely on ...
Recent work has shown that ...
```

#### 3. Point out the problem or gap

The third part is the heart of the Introduction. It answers: given all this prior work, why is this paper still needed?

You can point out that:

- existing methods still fail in a certain class of scenarios;
- existing benchmarks cannot accurately evaluate a certain capability;
- current data, models, or theory have limitations;
- prior work overlooked an important variable;
- current conclusions are inconsistent;
- a problem still lacks systematic study;
- …

This paragraph must be specific. Do not just write "However, this problem remains challenging." Say exactly where the difficulty lies.

Better ways to put it:

- In which scenarios does it fail?
- Which assumption does not hold?
- Which capability is not being measured?
- Which cost is too high?
- Which kind of data is missing?
- Which mechanism is still unclear?

Useful sentence patterns:

```
However, little is known about ...
Nevertheless, existing methods still suffer from ...
Despite these advances, ... remains unclear.
A key limitation of current approaches is ...
To date, few studies have systematically examined ...
```

#### 4. Introduce this paper

The fourth part answers: what does this paper actually do?

It usually covers:

- the goal of the paper;
- the method or the object of study;
- the main contributions;
- how it differs from prior work;
- a brief outline of the paper, if needed.

Note: this part must be clear and direct — stop setting up.

You can write:

```
In this paper, we propose ...
Here, we investigate ...
We introduce a new benchmark for ...
Our approach differs from previous work in ...
The main contributions of this work are ...
```

### 11.2　Paragraph organization

One paragraph carries one core point, and the first sentence of each paragraph — the topic sentence — must tell the reader what that paragraph is about; the rest of the paragraph develops it (discussion, examples, description).

A standard Introduction can be organized in 4–6 paragraphs:

#### Paragraph 1: broad background

State the importance of the field and the basic problem.

#### Paragraph 2: prior work

Summarize existing methods, data, theory, or systems.

#### Paragraph 3: limitations and gap

Point out the limitations of prior work and narrow the problem down to this paper's focus.

#### Paragraph 4: this paper's method

State what method, system, dataset, benchmark, or theoretical analysis this paper proposes.

#### Paragraph 5: contribution summary

List 2–4 contributions. Each must be concrete and verifiable.

#### Paragraph 6: paper structure

Optional. Some journals and long papers require it; ML conference papers usually omit it.

### 11.3　A reusable skeleton

**Paragraph 1:**

In recent years, the problem of ... has become increasingly important in ... . The core of this problem lies in ... , which is significant for ... .

**Paragraph 2:**

Prior work has mainly addressed this problem from the angle of ... . For example, ... focuses on ... , while ... further ... . These efforts have advanced ... .

**Paragraph 3:**

However, existing research still has a key limitation: ... . Specifically, ... . Consequently, in ... scenarios, existing methods struggle to ... .

**Paragraph 4:**

To address this, this paper proposes ... . We design / construct / analyze ... , and validate its effectiveness through ... .

**Paragraph 5:**

The main contributions of this paper are: first, ... ; second, ... ; third, ... .

---

## 12 · How to Write Related Works

> **Note**　In the original handbook this chapter is an interactive page whose body could not be captured. The points below are compiled from criteria in the other chapters and from common reviewer complaints.

Related Works is not a literature review. Its only job is to **set up this paper's gap**: after reading it, the reviewer should believe that the problem really is unsolved.

Four parts:

1. **Categorize**: split prior work into 2–4 groups by methodological paradigm (not by year or by author), and name each group.
2. **Representative work**: pick 2–4 of the most representative papers per group and state each core idea in one sentence.
3. **Limitations**: every group must end on "what this group cannot solve", measured with the same yardstick so the groups are comparable.
4. **Positioning**: the final paragraph states how this paper differs — which group it belongs to, and which point it breaks through.

Three hard criteria:

- **Categories must be orthogonal**: do not put "CNN-based methods" and "attention-based methods" side by side when they overlap.
- **Praise without critique is not writing**: every citation must carry an evaluation, and the evaluation must point at the gap this paper fills.
- **Divide the work with the Introduction**: the Introduction cites only 3–5 works that establish motivation; Related Works does the full comparison. Never repeat the same paragraphs in both.

Common failure modes:

- A laundry list — "A proposed … B proposed … C proposed …" — after which the reader neither knows who is stronger nor what is missing.
- Missing the reviewer's own paper, or missing the most direct competitor — a frequent reason for rejection.
- Framing this paper as "one instance of an existing category", which gives away the right to define its novelty.

---

## 13 · How to Write Methods

> **Tip**　Methods is usually the easiest part to write, because it answers one question:
>
> how exactly does the method work?
> For an AI paper, Methods usually has to make the following clear:
> - the core idea of the method
> - the problem definition and notation
> - the model architecture or algorithm flow
> - the design rationale of each key module
> - the formulas, objective function, and derivations

### 13.1　Use a general-to-specific structure

> Figure 13-1　The general-to-specific structure of Methods (schematic, from the original). Key points: Overview: core idea + division of labor across modules + flow from input to output / Problem | Method | Training / | Inference / / Formulation | Details | Optimization | Deployment / ↑ from coarse to fine: first let readers see what the whole does, then why each module is designed that way / the main figure is for *seeing* the method, the Overview is for *reading* that figure — they must come as a pair

Methods usually works best general-to-specific:

- **Overview**: introduce the method as a whole.
- **Problem Formulation**: define the problem and the notation.
- **Method Details**: explain the method module by module.
- **Training / Optimization**: state the training objective and how it is optimized.
- **Inference / Deployment**: explain how it runs at test or deployment time.

The benefit: readers see the whole method first and move into details gradually, instead of being flooded by formulas, symbols, and module names at the start.

### 13.2　Write the Overview first

Methods usually opens with an Overview paragraph introducing the core idea.

The Overview needs no detail; it answers:

- What problem does the method solve?
- What is its starting point?
- Which main modules does it consist of?
- What is each module roughly responsible for?
- How does the whole pipeline go from input to output?

The Overview should be paired with the method figure: the figure lets readers *see* the method, and the Overview lets them *read* that figure.

### 13.3　Write a separate Problem Formulation

AI papers are full of letters, symbols, variables, sets, functions, and subscripts. Without clear definitions up front, reading the formulas later is painful.

So write a separate Problem Formulation subsection.

It should state:

- what the input is;
- what the output is;
- how the training data is represented;
- how the model or function is represented;
- what the objective is;
- what the key variables, sets, indices, and symbols mean.

### 13.4　Every formula must be explained

Every formula in Methods should meet three requirements:

- Before the formula, explain why it is needed.
- After the formula, explain each key symbol in it.
- After the formula, explain what role it plays in the method.

Never drop a formula on the reader and let them guess its meaning.

The recommended pattern is: one lead-in sentence,

```
To model ..., we define ...
```

then the formula, then the explanation,

```
where ... denotes ..., and ... represents ....
```

and finally its role:

```
This objective encourages the model to ...
```

In particular:

- Define every symbol the first time it appears.
- Do not use the same symbol for different meanings in different places.
- Do not add unnecessary subscripts.
- Formulas should be tied to the argument, not added to look "mathematical".

### 13.5　Expand Method Details module by module

After the Overview, the body expands the method module by module.

If the method has three modules, write:

```
Module A: ...
Module B: ...
Module C: ...
```

For each module, follow this order:

- What problem does this module solve?
- What input does it take?
- How does it process the input?
- What does it output?
- Why is it designed this way?

Do not write only module names and formulas. What readers need is what function the module serves in the whole method.

### 13.6　Use pseudocode for complex procedures

If the pipeline is complex, add an Algorithm block or pseudocode.

Pseudocode must not replace the prose explanation. The right pattern:

- The text first explains the purpose of the algorithm.
- The pseudocode shows the full procedure.
- The text then explains the key steps and the design rationale.

Variables in the pseudocode must be consistent with the symbols in the text.

### 13.7　State the novelty clearly

Methods must not only describe the method but also tell readers where the novelty lies.

In each key module you can state:

- how this module differs from existing methods;
- why this design is needed;
- what specific problem it solves;
- what happens without it.

Keep the novelty statements in Methods brief — detailed comparison and evidence belong in Experiments.

---

## 14 · How to Write Experiments

### 14.1　A typical structure

- Experimental Setup
- Main Results
- Ablation Study
- Analysis / Further Study
- Case Study / Visualization
- Robustness / Generalization
- Efficiency / Cost Analysis

Not every paper needs all of them. The structure should serve the contributions, not pad the experiment count.

### 14.2　Write Experimental Setup first

Experimental Setup is the foundation: it tells readers under what conditions the experiments were run.

It usually covers:

- which datasets / benchmarks are used;
- which baselines are compared;
- which evaluation metrics are used;
- the implementation details of the model;
- training and inference hyperparameters;
- the number of runs, random seeds, and how statistics are computed;
- whether all methods were compared under fair conditions.

This part must be clear and concrete; move excessive detail to the appendix.

### 14.3　Main Results must serve the core claim

Main Results is usually the most important part of Experiments and corresponds to the main table and figure.

It answers:

- Does this method beat existing methods?
- On which datasets or tasks is the gain clear?
- Which results best support the paper's contribution?
- Are there cases with no gain or only a small gain?

Do not just write "Table 1 shows the results"; tell readers what to look for.

Recommended pattern:

```
Table 1 compares our method with existing baselines on ... . Our method achieves the best performance on ... , suggesting that ...
```

### 14.4　Ablation Study explains why the method works

The job of an ablation study is to prove that the key modules or design choices are not arbitrary additions but genuinely useful.

Common ablations:

- remove a module;
- replace a module;
- change a training objective;
- change the prompt / retrieval / memory / ranking strategy;
- change data volume or training configuration;
- compare model sizes or parameter settings.

Write ablations around the design rationale:

```
To evaluate the contribution of ..., we remove ... and compare the resulting model with the full model.
```

### 14.5　Analysis deepens understanding

Beyond main results and ablations, many papers need an Analysis section explaining the method's behavior.

Common analyses:

- performance on different categories of samples;
- performance on tasks of different difficulty;
- performance under different data volumes;
- trends across model sizes;
- the distribution of error types;
- sensitivity to hyperparameters;
- sensitivity to prompts, number of retrieved items, context length;
- agreement with human performance or expert annotation.

The goal of Analysis is not to repeat the main table but to help readers understand:

> **Tip**　When is the method better? Why is it better? When is it not good enough?

### 14.6　Case study and visualization

If the method or task is complex, add a case study or visualization.

Case studies suit situations where:

- results are hard to convey with numbers alone;
- you need to show the quality of model outputs;
- you need to compare the behavior of different methods;
- you need to show failure cases;
- you need to convey the difficulty of the task.

### 14.7　Details that matter

- **Invite readers to the figures and tables.** Never assume they will look on their own; guide them explicitly:
- Figure 1 shows the results...
- As can be seen in Fig. 1...
- The results are summarized in Table 1...
- **Describe the key results.** Choose the important, typical, or especially interesting results and describe them in detail; do not treat every result equally. Whatever you choose to describe, readers will take as important.
- **Use evaluative language.** Do not let raw numbers speak for themselves; tell readers what the numbers mean.
- **Acknowledge problems and anomalies.** If results contain flaws, anomalies, or data that do not match expectations, do not hide them — but soften them with hedged language:
  - ❌ Beginner: say nothing about the anomaly → looks like someone who did not notice the problem.
  - ✅ Expert: "Although the average uncertainty slightly exceeds the 50% acceptability limit, nevertheless these results suggest that..." (acknowledge + soften + pivot to the positive)
  - Common hedges: slightly, somewhat, only approximate, a minor deficit, negligible, not significant, it should be noted that...

---

## 15 · How to Write References

> **Tip**　References must not be copied from Google Scholar or DBLP and pasted in as they are. Every single entry must be edited by hand to make the format correct and consistent.

### 15.1　Steps for organizing references

1. Copy the bib entry from DBLP.

2. Unify the key: author surname + year + keyword, for example

```
@inproceedings{zhou2024symagent,
```

not `@inproceedings{DBLP:conf/icml/ZhouL24`.

3. Fix the entry type: `@inproceedings` for conferences, `@article` for journals.

4. Delete useless fields such as `publisher`. In general these fields are enough:

> **Tip**
>
> - author
> - title
> - booktitle / journal
> - volume (journals)
> - number (journals)
> - pages
> - year

5. Protect capitalization. A bib entry copied directly will lowercase what should be uppercase; protect it with braces.

For example, `title={{SymSkill}: Symbol and Skill Co-Invention for Data-Efficient Robot Learning}` — without braces everything becomes lowercase. Protect paper titles and common names such as LLM and GPT in braces, for example:

```
title = {{GPT}-4o mini}
title = {{Qwen3}-8B}
title = {{LLM-SR:} {S}cientific Equation Discovery}
```

6. **Author**: unless there are too many authors, keep them all; if there really are too many, use et al. The author format exported by DBLP can be kept as is — no need to rewrite it.

7. **booktitle / journal**:

8. Make sure the format of every citation to the same conference is exactly identical — do not mix full names with abbreviations, or capitalized with uncapitalized forms.

9. For most conferences write `Proceedings of the xxth International Conference on Machine Learning`. Note:

10. Write the edition as a number and use the correct ordinal: 1st, 2nd, 3rd, 4th, 5th…

11. Some conferences have a year instead of an edition; just keep the format consistent within that conference, for example:

12. EMNLP: {Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing}

13. CVPR: `booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition}`

14. Some conferences have no "Proceedings"; just keep the format consistent, for example:

15. NeurIPS: `booktitle = {Advances in Neural Information Processing Systems}` (note that NeurIPS citations often carry a number, e.g. "Advances in Neural Information Processing Systems 34" — delete the 34)

16. Capitalize the first letter of every word in the conference name.

17. **Volume / Number**: journal citations need the exact volume and issue, for example:

```
journal={Nature},
volume = {529},
number = {7587},
pages = {484--489},
year={2016}
```

18. **Pages**: keep them for everything except venues without page numbers, such as ICLR.

### 15.2　Pre-submission checklist

1. Are irrelevant fields such as Publisher and URL deleted?

2. **Title**: is capitalization mixed — some titles with every word capitalized, others with only the first letter?

3. **Author**: are names complete, replaced by et al. when too many, and consistently capitalized?

4. **Booktitle / Journal**: is the format consistent within a venue, free of stray words (such as the NeurIPS number), and consistently capitalized?

5. **Volume / Number**: are volume and issue present for journal citations?

6. **Pages**: are page numbers present except for venues such as ICLR that do not have them?

7. Are there duplicate entries?

---
