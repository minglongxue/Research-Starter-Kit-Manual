# 科研入门手册 · PDF 精排版 + WorkBuddy Skill

> 把 [**LAMDA-NeSy/Research-Starter-Kit**](https://github.com/LAMDA-NeSy/Research-Starter-Kit)（《科研入门指南：从 0 开始，掌握做科研、写论文的基本流程》）整理成一份可离线阅读、可打印、目录可跳转的 PDF，并打包成两个中英文 WorkBuddy Skill。
>
> **本仓库是非官方衍生整理版，全部内容版权归原作者所有。请先读下面的致谢。**

---

## 🙏 致谢原作者

**这份手册的每一句内容都属于原作者，本仓库只做了排版与打包。**

- **作者：[郭兰哲](https://www.lamda.nju.edu.cn/guolz/)** — 南京大学智能科学与技术学院准聘副教授、博士生导师，[LAMDA](https://www.lamda.nju.edu.cn/) 课题组。研究方向：智能体（Agent）、世界模型（World Model）、大模型推理（LLM Reasoning and Planning）、神经符号学习、表格数据大模型。
- **原项目：[LAMDA-NeSy/Research-Starter-Kit](https://github.com/LAMDA-NeSy/Research-Starter-Kit)** — 目前 **10.2k+ Star**、380+ Fork，是中文科研入门领域影响最广的开源资料之一。
- **共同参与编写的同学**：陈煜旸、葛凌岳、张逸凯（据原项目 README 致谢）。

> 👉 **如果你觉得这份资料有价值，请把 Star 给[原项目](https://github.com/LAMDA-NeSy/Research-Starter-Kit)，而不是这里。**
> 原项目仍在持续更新，内容以原项目为准；本仓库只是某一时点的排版快照。

原项目 README 中列出的参考与借鉴资料，在此一并致谢：

- 周志华老师：[做研究与写论文](https://zhuanlan.zhihu.com/p/98747105)
- 凌晓峰 / 杨强：《学术研究，你的成功之道》
- 浙江大学 彭思达老师：[我的科研经验](https://github.com/pengsida/learning_research)
- 东南大学 魏秀参老师：[浅谈学术 Rebuttal](https://zhuanlan.zhihu.com/p/104298923)
- [MLNLP-World / Paper-Rebuttal-Tips](https://github.com/MLNLP-World/Paper-Rebuttal-Tips)
- 《Science Research Writing: For Non-Native Speakers of English》

---

## 📥 下载

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| [**科研入门手册（中文·精排版 PDF）**](./manual/Research-Starter-Kit-Manual-ZH.pdf) | 57 页，A4，目录可跳转、带书签与页码 | 8.6 MB |
| [**research-starter-kit.zip**](./dist/research-starter-kit.zip) | 中文版 WorkBuddy Skill | 47 KB |
| [**research-starter-kit-en.zip**](./dist/research-starter-kit-en.zip) | 英文版 WorkBuddy Skill | 42 KB |

> GitHub 页面上的「Download raw file」按钮即可下载；也可以直接用 `curl -L` 拉取 raw 链接。

---

## 📖 这份 PDF 做了什么

原手册是飞书文档，在线阅读体验不错，但**离线保存、打印、翻页检索都不方便**：导出 PDF 会丢图、目录没有页码、长表格被截断。所以重新排版了一版：

**结构**
- 全文 **19 章 / 4 篇**（上篇：如何做科研 · 中篇：如何写论文 · 下篇：学术生活 · 附录），**57 页**
- 封面 → 目录（带页码、按篇章分组）→ 各章 → 附录 A 参考文献
- **22 条 PDF 书签**，侧栏可直接跳章；目录 **24 个内部链接**可点击

**排版**
- 每章独立起页，章号大字号做视觉锚点，章首标注所属篇章
- 标题层级重新建立（h2 宋体大字 / h3 紫色左竖条 / h4 方块标记 / h5 标签 chip）
- 正文 14px / 行高 1.75，每章首段升为「导语段」加深墨色
- 主色深紫 `#5B2A63`，强调色暖橙 `#B4622A`；提示块用米色底 + 橙色边，与正文明确区分
- 每页页眉（书名 + 当前章名）与页脚页码

**内容还原**
- 第 09 章《论文画图指南》与第 10–16 章「如何写论文」系列（Abstract / Introduction / Methods / Experiments / Reference / Rebuttal），均按**作者提供的 Word 原稿全文重排**，**35 张原始配图完整保留**
- 第 17 章《学术会议参会指南》、第 18 章《奖学金》同样按 Word 全文重排：参会指南做成「准备—交流—整理—心态—清单」五节 + 三档自我介绍 + 会后邮件模板；奖学金 21 个项目编译成「名称 / 时间窗 / 对象与金额 / 官网」速查卡
- 表格统一紫底白字表头 + 斑马纹，代码块与 bib 条目等宽排版

**体积**
- 17 MB → **8.6 MB**：仅把 35 张无损 PNG 截图转 JPEG（质量 86）并按实际版面尺寸重采样到 190 dpi；文字、矢量、链接一个字节未动，逐页像素比对确认无内容缺失

---

## 🧩 WorkBuddy Skill

把手册做成 Claude / WorkBuddy 可加载的 **Skill**，写论文、画图、回 Rebuttal 时可直接调用其中的判据，而不是让模型自由发挥。

```
research-starter-kit/              # 中文版
├── SKILL.md                       # 路由表 + 三原则 + 各节硬判据 + 自检清单
└── references/
    ├── 01-research-workflow.md    # 第 01–07 章：找论文、读论文、想 Idea、汇报、Meeting、习惯
    ├── 02-paper-writing.md        # 第 08、10–15 章：Abstract → Reference 全流程
    ├── 03-paper-figures.md        # 第 09 章：论文画图指南
    ├── 04-rebuttal.md             # 第 16 章：Rebuttal 战术
    └── 05-academic-life.md        # 第 17–19 章 + 附录
```

英文版 `research-starter-kit-en/` 结构与内容一一对应，界面语言为英文。

**设计要点**：手册 3.5 万字全部塞进 `SKILL.md` 会超载（Skill 正文常驻上下文），所以按渐进式披露拆分——主文件只留「什么问题读哪个文件 + 最硬的判据」，细节放 `references/` 按需加载。

**安装**

```bash
# 用户级（所有项目生效）
unzip research-starter-kit.zip -d ~/.workbuddy/skills/

# 或项目级（仅当前工作区）
unzip research-starter-kit.zip -d <项目目录>/.workbuddy/skills/
```

注意 zip 内已含一层同名目录，不要解压成 `skills/research-starter-kit/research-starter-kit/`。装好后重开会话生效，用自然语言即可触发，例如：

- 「帮我看看这段摘要的问题在哪」
- 「teaser 图怎么排」
- 「审稿人说 novelty 不足怎么回」

---

## ⚠️ 与原版的差异（重要）

为了让内容可信，这里明确列出**哪些是原文、哪些是整理者所加**：

1. **排版全部重做**，文字内容按 Word 原稿逐段还原，未改写、未删减原有观点。
2. **第 12 章《Related Works》**：原手册该页为交互式组件，抓取与导出均无法获得正文。PDF 与 Skill 中这一章的四段结构建议与三个常见问题，**是整理者依据其余章节判据补写的，已在文中明确标注为「整理补充，非原文」**。
3. **上篇第 01–08 章的插图**：原图为飞书 canvas 渲染，无法提取，因此由整理者依据原文逻辑重绘为**示意图**，文中均已标注「示意图，不替代原图」，准确信息请回看原项目链接。第 09 章之后为作者 Word 原稿中的原图。
4. 修正了若干解析缺陷（如步骤列表被代码块切成多个「1.」、表格内嵌 Excel 预览图丢失、链接被自动识别吞掉全角括号等），属排版修复，不涉及内容改动。

**若发现任何与原意不符之处，一律以[原项目](https://github.com/LAMDA-NeSy/Research-Starter-Kit)为准，并欢迎提 Issue 指正。**

---

## ⚖️ 版权与使用限制

- 原项目 **未声明开源许可证（no license）**，即默认保留所有权利。因此：
  - 手册**文字与图片内容的著作权归郭兰哲老师及参与编写的同学所有**；
  - 本仓库仅作**个人学习、离线阅读与非商业性分享**用途，**不得用于任何商业目的**；
  - 本仓库与原作者**无隶属关系，也未获正式授权**，属社区整理行为；
  - **如原作者认为本仓库不妥，请提 Issue 或联系，会立即删除。**
- 整理者新增的部分（PDF 排版文件、Skill 的目录结构与判据速查编排）采用 MIT 许可，可自由使用。
- 引用本手册内容时，请引用原项目：

```
郭兰哲等. 科研入门指南：从 0 开始，掌握做科研、写论文的基本流程.
GitHub: LAMDA-NeSy/Research-Starter-Kit, 2026.
https://github.com/LAMDA-NeSy/Research-Starter-Kit
```

---

## 🔧 自行构建

PDF 由 HTML 经 Edge 无头打印生成，再用 PyMuPDF 补齐页眉页脚、书签与目录页码：

```bash
# 1. 生成 HTML（合并基础版 + Word 重排章节）
python 生成第9章.py && python 生成第10-16章.py && python 生成第17-18章.py

# 2. 注入 v2 样式并构建 PDF（两遍导出回填目录页码）
python build2.py

# 3. 压缩到 10MB 以内
python -c "import pymupdf; d=pymupdf.open('out.pdf'); \
d.rewrite_images(dpi_threshold=400, dpi_target=190, quality=86, lossy=True, lossless=True); \
d.save('out-min.pdf', garbage=4, deflate=True, clean=True)"
```

Skill 由 `extract_refs.py` 从构建后的 HTML 抽取为 Markdown（保留代码块、表格、卡片与 SVG 图示文字）。

---

## English

This repository hosts an **unofficial, reformatted derivative** of [LAMDA-NeSy/Research-Starter-Kit](https://github.com/LAMDA-NeSy/Research-Starter-Kit) — a highly regarded Chinese-language handbook on doing research and writing papers, maintained by [Prof. Lan-Zhe Guo](https://www.lamda.nju.edu.cn/guolz/) (Nanjing University, LAMDA).

**All credit for the content belongs to the original authors.** This repo only contributes:

- a 57-page A4 PDF rebuilt from the authors' Word sources (clickable TOC, 22 bookmarks, headers/footers, all 35 original figures), compressed from 17 MB to 8.6 MB;
- two ready-to-install WorkBuddy/Claude skills (Chinese and English) that expose the handbook's judgment criteria, checklists and templates.

The original project carries **no license file**, so the handbook text and figures remain all rights reserved by their authors. This repo is for personal study and non-commercial sharing only. If the original authors object, it will be taken down immediately.

If you find this useful, please **star the [original project](https://github.com/LAMDA-NeSy/Research-Starter-Kit)**.
