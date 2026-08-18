# Linear Algebra Done Wrong — 中文翻译项目

本项目是 Sergei Treil 教授教材 **Linear Algebra Done Wrong** 的中文翻译与中文排版工程，也是南京大学匡亚明学院线性代数课程学习过程中逐步维护的一份译稿。

当前开发线以作者 **2026-04-30** 版本为英文内容基准，目标是在忠实数学内容和原书结构的前提下，保留译者自己的中文表达、术语习惯和必要的译者注。

## 当前版本与来源

本轮 2026 校订以 Sergei Treil 教授于 **2026-04-30** 发布的官方版本为英文内容基准：

1. 正文、定理、公式、习题与章节结构均直接对照作者官方 LaTeXML 页面校订。
2. 为方便逐章、逐公式核对，维护过程中会将官方网页整理为本地结构化工作稿；这只是校订工具，并非作者公开的原始 LaTeX 源文件。
3. 中文部分以本项目既有译稿为基础，并直接依据官方英文版本持续校订、重译和润色。
4. 正文插图优先使用矢量 PDF / TikZ 版本；对于作者官方网页中的图形，仅将网页内容作为核对依据，不使用网页栅格化图片替代已有矢量图。

更完整的来源约束见 [`TRANSLATION_PROVENANCE.md`](TRANSLATION_PROVENANCE.md)。

## 项目特点

- **对应 2026 原书结构**：章节、小节、定理族、习题和公式的结构已按官方 2026 页面校准。
- **独立中文表达**：保留原译稿的语言风格和译者注，同时直接对英文重新审校有问题的段落。
- **自动交叉引用**：正文逐步由旧式手写编号迁移到 `\label` / `\ref` / `\eqref`，减少改版后的错号风险。
- **专业 LaTeX 排版**：正文使用 XeLaTeX；包含目录、交叉引用、中文索引和译者习题解答附录。
- **可审计的项目历史**：废弃的早期草稿放入 `legacy/drafts/`，不参与正式构建。

## 目录结构

```text
main.tex                     主文件
zhbook.cls                   中文书籍样式与编号设置
part/chap01.tex ... chap09.tex  正文九章
part/preface.tex             推荐序、译者的话、作者前言
part/exercises.tex           译者整理的习题解答附录
figures/                     项目插图
legacy/drafts/               不参与构建的历史草稿
TRANSLATION_PROVENANCE.md    翻译来源与校订说明
```

## 自行编译

建议使用完整的 TeX Live / MacTeX / MiKTeX 环境，并确保 XeLaTeX 与索引工具可用。

最基本的正文/目录/交叉引用编译流程：

```bash
xelatex main.tex
xelatex main.tex
```

若需要生成索引，按本项目现有索引工具配置运行 `makeindex` / `zhmakeindex` 后，再运行两次 XeLaTeX。典型流程为：

```bash
xelatex main.tex
makeindex main
zhmakeindex main
xelatex main.tex
xelatex main.tex
```

仓库当前版本可以正常完成 XeLaTeX 编译，并生成包含目录、交叉引用、中文索引和习题解答的完整 PDF。

## 如何贡献

欢迎提交：

- 数学错误、公式/下标错误；
- 对照英文原文发现的漏译、误译；
- 中文表达和术语一致性建议；
- LaTeX 编译、排版、索引与交叉引用问题；
- 习题解答中的错误或更好的解法。

对于正文翻译贡献，请尽量直接注明所依据的英文原句/所在章节，以便维护翻译来源的可追溯性。

## 致谢

- Sergei Treil 教授：原书作者。
- 南京大学匡亚明学院李耀文老师：课程与反馈是项目启动和持续维护的重要契机。
- `zhbook` 项目：本项目中文 LaTeX 版式的基础之一。
- 所有参与勘误、反馈和改进的同学。

## 许可与版权说明

仓库中的模板、辅助代码等项目代码可以按仓库自身的 `LICENSE` 处理；**不要据此推断 Sergei Treil 的原作文字、公式编排或中文翻译也自动适用 MIT License**。

本项目用于校订的官方 2026 页面标示原作为 **CC BY-NC-ND 3.0**。原作内容、译文及其公开发布应分别遵守适用的原作许可、作者/译者权利与必要授权。本 README 不把仓库代码许可证扩张解释为对原作或译文内容的授权。

## 联系方式

- GitHub 项目：`DongYaoZe/Translate-LADW`
- 邮箱：`yzdong@smail.nju.edu.cn`

欢迎勘误和改进建议。
