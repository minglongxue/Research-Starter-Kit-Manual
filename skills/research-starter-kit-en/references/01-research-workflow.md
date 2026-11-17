This file covers the onboarding stage: how to think about research, finding papers, reading papers, generating ideas, academic presentations, running efficient meetings, and daily habits.

## 01 · How to Do Research

> Figure 1-1　The research loop (schematic, based on "main tasks of a graduate student"). Key points: research is a closed loop — a problem found at any stage sends you back to the previous one / Find papers | Read papers | Generate ideas | Run experiments | Write the paper | Submit / Understand the field | Read critically | Find the real problem | Validate feasibility | State the contribution | Rebuttal / Rejection or reviews → add experiments or reframe → back to "generate ideas"

### What research is

Broadly, research produces original and influential contributions to human understanding through reproducible observations and verifiable results. In AI this includes, but is not limited to:

1. **Discovering new knowledge**: new theory, new model architectures, new algorithms.
2. **Solving new problems**: using new techniques, designs, methods, or models to address real problems.

### Judging novelty and impact

If the work is only a straightforward derivation or incremental improvement over existing work (which describes most students' work), its novelty and impact are usually limited. A highly influential paper typically has one of these traits:

- **It attacks a key problem in the field's development** and offers a new method with a large advantage over existing ones — e.g., ResNet mitigating vanishing gradients in deep networks, Transformer mitigating RNNs' long-range dependency and parallelism problems.
- **It lays the groundwork for later work or opens a new direction** — e.g., GAN introducing a new paradigm for image generation.
- **It shows a decisive advantage on a recognized task** — e.g., AlexNet winning ImageNet, AlphaGo beating professional players.

### What a graduate student actually does

1. **Explore and formulate new ideas**, ensuring novelty: track the state of the field and do extensive literature search and reading.
2. **Turn ideas into experiments** to test feasibility: this requires rigorous experimental analysis and fast coding.
3. **Write and submit**: AI papers usually go to conferences and are decided by peer review and rebuttal; writing and presentation skills must keep improving.
4. **Review others' papers**: conferences require authors to also serve as reviewers — a role reversal that trains you to judge others' novelty and impact.
5. **Attend conferences**: present your work, learn new results, exchange ideas, find collaborators.
6. **Apply for scholarships and funding**: much funding targets graduate students and even undergraduates, and it helps with network, visibility, and living costs.
7. **Help supervise junior students**: senior PhD students mentor newcomers alongside their advisor — an extra required course of the PhD.
8. **Take part in project development**: join funded projects and apply research results to real settings.

---

## 02 · How to Find Papers

1. **Start from major conferences and journals.** AI publishes mainly at conferences. After each conference's decisions are released, the full paper list is available; for OpenReview venues you can also see all submissions. After every deadline and notification, screen and read the relevant papers once. Common venues:

| Area | Venues |
| --- | --- |
| Machine learning | ICML, NeurIPS, ICLR |
| Natural language processing | ACL, EMNLP, COLM |
| Computer vision | CVPR, ICCV, ECCV |
| Artificial intelligence | AAAI, IJCAI |
| Data mining and information retrieval | KDD |
| Broad high-impact journals | TPAMI, JMLR, TMLR, TKDE, Nature Machine Intelligence, etc. |

This list is neither fixed nor the only measure of a paper's value. Once you enter a specific area, build your own priority venue list based on your advisor's advice and the citation habits of the field.

2. **Expand from seed papers.** When entering a new area, first find a few "seed papers" and expand around them. Good seeds are usually:

   - high-quality surveys from recent years;
   - the recognized representative work of the area;
   - the papers closest to your own research question;
   - widely used benchmark papers;
   - representative papers from the last two years of top venues;
   - papers recommended by your advisor or peers.

3. **Follow the citation network.** Reading a paper is not reading one paper: use its Introduction, Related Works, compared methods, and references as entry points to more work.

   - **Backward tracking**: which earlier work does it cite?
   - **Forward tracking**: which later work cites, improves, challenges, or extends it?

4. **Track authors, groups, and teams.** While reading, note which group the authors belong to. If a group works on your topic, they likely have a series of related papers and students in that direction.

---

## 03 · How to Read a Paper

> **Tip**　Every topic's history is paved with the intelligence and effort of many people, and there is always a thread connecting it end to end. One day, when the scattered pieces in your head line up into a single thread, everything suddenly clicks — "ah, so that's how it is!" That is when research starts to be fun.

### The seven-step method

> Figure 3-1　Steps for reading a paper (schematic; the original calls it a seven-step method, six steps were captured here — see the original link for the full version). Key points: Macro overview / 1 / Read the abstract and skim figures first: what type of work is this, what problem does it solve / Pin down the core research question / 2 / It may be in the abstract or buried at a turn in the introduction — find it first / Map the existing work / 3 / How did others solve it? What is still missing? How would I do it? / Read the proposed method / 4 / Compare the authors' solution with yours, critically / Analyze and reproduce experiments / 5 / Are datasets, baselines, and metrics fair and complete? Reproduce key papers from code / Follow the thread / 6 / Expand through introduction, related works, and references to the whole background

1. **Macro overview.** Do not read word by word from the start. Skim the abstract and figures first to build a basic picture: who published it, what type of work it is, what problem it solves, roughly how well it works.
2. **Pin down the core research question.** A paper's core is the question it answers. Good papers revolve around one clear, specific question — sometimes in the abstract, sometimes at a turn in the introduction. Find it first.
3. **Map the existing work.** Ask actively: is this problem real? Who has studied it? What are the current solutions? What challenges remain? If it were my project, what would I do?
4. **Read the proposed method.** Scrutinize it and compare the authors' solution with the one you imagined. Look for limitations critically, mine them for new ideas, and think about how to improve and surpass it.
5. **Analyze and reproduce experiments.** Which datasets? Which baselines? Is the setup complete? Are the conclusions sound? Is code available? For key papers, read the code and try to reproduce.
6. **Follow the thread.** Use the paper as a lead, combined with its introduction, related works, and compared methods, to understand the whole research background, and learn the techniques, methods, and concepts you have not yet mastered.

---

## 04 · How to Generate Ideas

Idea generation has two steps: **choose a good research problem**, then **find a solution**.

### Problem-driven vs. method-driven

- **Problem-driven research**: find an important problem or goal and figure out how to solve it well. For example, if LLMs perform poorly on some task, fix one or two benchmarks and explore techniques until the task works; or build a new benchmark to define a problem clearly (e.g., in game agents, when no benchmark supports a certain evaluation, define one); or analyze an existing solution on a general benchmark to find the key challenge (e.g., GRPO's efficiency or credit-assignment problems) and then improve it.
- **Method-driven research**: hammer in search of a nail — keep applying an existing technique to new problems. For example, applying GRPO to multimodal reasoning or agentic RL as soon as it appeared; applying a hot technique to math, medical, or legal domains.

> **Tip**　The two approaches often need to be combined. In most cases problem- (goal-) driven research is preferable, adapting and optimizing the method along the way.

### How to find a research problem

1. **Read papers critically.** Pick holes while reading, think about what the paper does not handle, and fuse "reading" with "questioning" rather than separating them into two phases — actively ask "what if I change the data or the assumption?" Develop this habit as early as possible: many students read a great deal in their first two years yet cannot pose a question, precisely because they only *understand* and never *doubt*.
2. **Look for opportunities in failures.** Ask which failure cases the mainstream approach has, actively find and reproduce them, analyze the causes, and try to propose a solution.
3. **Reverse-engineer the mechanism from "does it work, and why".** For methods that work well but lack explanation, ask what is actually happening inside and why it works, and run experiments to analyze the algorithm. Such reverse-engineering questions are often easier to enter than "design a new method": you already have a confirmed effective phenomenon as an anchor, and only need to design experiments or theoretical tools to take it apart.

---

## 05 · How to Give an Academic Talk

### Format (slides)

Slides do not need flashy animation, but they must look decent:

- Consistent, sensible fonts: for Chinese use Microsoft YaHei or YouYuan; for English use Calibri, Times New Roman, etc.
- Sensible sizes and spacing: title 32–36 pt, body 18–24 pt, line spacing 1.2–1.5.
- No walls of text: fewer than three lines per block (except important quotes); never read the slides aloud word by word.
- Highlight important parts with color or a background box.
- Include an outline page and section markers.
- Images may be AI-generated, but check that the content and logic are correct.
- For more, see Stanford's "How to Give a Good Academic Talk" (searchable on Bilibili).

### Content

1. **Pick a high-quality paper.** There are many AI papers, so make a value judgment: did you learn something new? What should the audience take away? Do you plan to follow this line of work?
2. **A tutorial on a direction is also fine.** Introduce new buzzwords and the development thread of a research direction.
3. **Stand in the audience's shoes.** A group-meeting talk should be understood by more than 80% of the room; add background knowledge depending on the audience.
4. **A thinking framework for the talk:**
   - **Overall contribution**: can you summarize it in 2–3 sentences? "For problem X, we propose method Y, achieving Z on task W."
   - **Motivation**: what problem does it solve? Is it a crowded problem or a new one? If crowded, how do related works divide into categories, and what is this paper's core advantage? If new, is it real or imagined? In what setting does it arise? What is the benefit of solving it? Is there a simple solution?
   - **Method**: what is the main pipeline? How many steps from input to output? How does the system run? Which modules does it contain?

---

## 06 · How to Run Efficient Meetings

### Why meet

- Meetings exist to push research forward efficiently, not to report progress. Research involves trial and error and stalled weeks — do not treat meetings as pressure.
- The goal is not to "prove you did a lot" but to **surface problems, clarify thinking, get feedback, and move the work forward**.
- Beyond regular meetings, book time whenever there is something to discuss, and build the habit of discussing problems as they arise.

### Format

1. **For an active project**: meet per project, with the project lead coordinating schedules. Each project keeps one document: what to do, technical contribution, timeline, division of labor, current progress, experimental results, and open problems — keep it to the point, not an essay.
2. **For individual learning**: keep a personal progress document — what you are following, papers you read (with the core point distilled), your own thinking, and discussions.
3. **Frequency**: at least every two weeks for an active project, and ad hoc when there are important results; at least every two weeks for PhD and master's students; at least monthly for interns and undergraduate interns.

### Meeting template (prepare before each meeting)

1. Review the project's overall direction and contribution, and reflect on whether you are on the right track.
2. Recall the conclusions and todos from the last meeting.
3. Summarize progress since then — in three sentences or fewer.
4. List the questions you want to discuss, plus interesting experimental phenomena and observations.
5. Share a few papers you recently read, each with a one-sentence summary.

---

## 07 · Good Habits

1. **Keep a steady input of research.** Spend 10–20 minutes before work browsing relevant arXiv categories, Hugging Face Daily Papers, conference paper lists, or academic platform recommendations to catch new papers, problems, and methods.
2. **Build your own knowledge system.** Store and manage valuable papers (inspiring ideas, strong results, good writing) with tools such as Zotero, Feishu, or multi-dimensional tables.
3. **Keep an experiment log.** For each important experiment record: purpose or hypothesis; what changed relative to the previous run; data, model, and hyperparameter configuration; random seed and runtime environment; core results; whether it matched expectations; current conclusion; next step. **Log failed experiments and negative results too** — they rule out wrong directions and stop you from repeating the same attempt weeks later.
4. **Log problems and solutions.** Record each problem and its fix to avoid re-debugging, and to help teammates. Even unsolved problems should be logged along with what you have already tried.

---
