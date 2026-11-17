This file covers the strategy, structure, and phrasing templates for responding to reviewers (rebuttal).

## 16 · How to Write a Rebuttal

### 16.1　Tactics and principles

- **Never drop a point.** Answer every comment one by one. If space is tight, merge similar comments into a single response — but never delete or silently omit a point to save space. Reviewers who notice a dodged question will treat it as a fatal flaw during paper discussion and use it against you.
- **Read the reviewer's inclination.** Co-opt everyone you can: the neutral can be won over, and even a hostile reviewer can be split off and managed. Some reviewers state outright, "if the authors address X, I will raise my score" — these must be fully satisfied. A weakness raised by one reviewer (e.g., novelty) is often praised by another ("This paper is interesting and novel"); use that quote so the two reviewers confront each other during discussion. For borderline reviewers, court them actively. For reviewers who gave a positive initial score, consolidate. For those who gave a negative score, spend the overwhelming majority of your effort and word budget explaining and clarifying, and try to win them back.
- **The rebuttal is one coordinated document.** It has to work together with the paper and with the reviews, and its word budget must be allocated deliberately: who gets more space, which issue deserves the deepest response — decide from the full set of reviews, not comment by comment.
- **Abbreviate aggressively.** Whatever can be shortened should be shortened, so the space goes to the responses that matter.
- **Strike first on factual errors.** If a reviewer makes an obvious factual mistake — a claim that is plainly wrong, or a demand to compare against a dataset that is not standard in this field — point out the error at the very start of your response to that reviewer and take the initiative. Remember that every reviewer and the AC can see the rebuttal. You may also raise it in the AC message to lower the weight the AC assigns to that review.

### 16.2　Common criticisms and how to answer

#### Insufficient novelty

Novelty complaints usually take two forms: (1) the method is not sufficiently different from prior work; (2) it is a simple A+B combination.

Re-organize and re-emphasize the paper's main contributions, clarify that this is not a trivial combination, and restate the motivation and intuition — express the highlights from a different angle.

A second route is to shift the ground: if the reviewer attacks the novelty of one component, emphasize that other components, or the paradigm of the whole method, are unprecedented; or argue that the method is simple yet effective, achieves strong results, and is SOTA.

#### Factual errors

These are hard to argue against. In most cases the only option is to concede gracefully, thank the reviewer, and state that the error will be corrected in the final version. If the misunderstanding came from your writing, you may concede and explain: "We have revised this description; what we actually do is X, not what you inferred."

#### Marginal improvement

- Cite prior work to show that your gain is comparable to the gains reported by other SOTA papers: "other papers published at top venues also improve over their baselines by this much."
- Look for settings where your method improves markedly, present them as a distinguishing feature, and argue that these settings matter. Alternatively, check whether the comparison was unfair and, if possible, add results under a fair setting: "the number they report was obtained under condition X; our setting is harder — under our setting their method degrades sharply."
- Point to other benefits: efficiency, generality, robustness, and so on.

#### Insufficient experiments

Add the experiments if you can. If you cannot, explain why — e.g., the scale is too large to run within the rebuttal window — and commit to including them in the final version. For unreasonable requests, explain honestly why the experiment is unnecessary and back the explanation with evidence such as references.

#### Grammar, structure, missing references

In most cases: acknowledge, thank, and fix.

### 16.3　AC message

If a reviewer is malicious, or makes factual errors you can point to, write a complaint to the AC.

If you find problems with a review — unprofessional, unfamiliar with the field, self-contradictory — you can use them to draw the AC's attention. Some possible phrasings:

```
Against common sense: Please note that Assigned Reviewer #id has made some statements that are either against the common-sense in our field or self-contradictory (ironically his/her own confidence rating is "very confident").
Self-contradictory: We want to bring to your attention the very flawed review #id. This reviewer is self-contradictory, cf. Comment #id1, Comment #id2, and Response #id. blabla
Strongly biased: We would like to raise attention to AC that unfortunately Reviewer #id holds a very biased view towards the contributions of our paper. blabla
```

### 16.4　Useful phrasing

Common sentence patterns for rebuttals, to pick from as needed:

**Opening**

```
Thank you for your suggestion.
Thank you for the positive/detailed/constructive comments.
We sincerely thank all reviewers and ACs for their time and efforts. Below please find the responses to some specific comments.
We thank the reviewers for their useful comments. The common questions are first answered, then we clarify questions from every individual review.
We thank the useful suggestions from the reviewers. Some important or common questions are first addressed, followed by answers to individual reviews.
```

**Agreeing**

```
We thank the reviewer for pointing out this issue.
We agree with you and have incorporated this suggestion throughout our paper.
We have reflected this comment by …
We can/will add/compare/revise/correct ... in our revised manuscript/our final version.
```

**Disagreeing**

```
We respectfully disagree with Reviewer #id that ...
The reviewer might have overlooked Table #id ...
We can compare ... but it is not quite related to our work ...
We have to emphasize that ...
The reviewer raises an interesting concern. However, our work ...
Thank you for the comment, but we cannot fully agree with the comment. As stated/emphasized ...
You have raised an important point; however, we believe that ... would be outside the scope of our paper because …
This is a valid assessment of …; however, we believe that ... would be more appropriate because ...
```

**Clarifying**

```
We have indeed stated/included/discussed/compared/reported/clarified/elaborated ... in our original paper ... (cf. Line #id).
As we stated in Line #id, ...
We have rewritten ... to be more in line with your comments. We hope that the edited section clarifies …
```

**Adding information**

```
We have included a new figure/table (cf. Figure/Table #id) to further illustrate…
We have supplemented the xxx section with explanations of ...
Thank you for the comment. We will explore this in future work.
```

### 16.5　Further reading

```
Rebuttal guide: https://github.com/MLNLP-World/Paper-Rebuttal-Tips
```

---
