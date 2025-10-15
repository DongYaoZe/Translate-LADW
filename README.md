# Linear Algebra Done Wrong - 中文翻译项目

[![GitHub stars](https://img.shields.io/github/stars/DongYaoZe/Translate-LADW?style=social)](https://github.com/DongYaoZe/Translate-LADW/stargazers)
[![Fork](https://img.shields.io/github/forks/DongYaoZe/Translate-LADW?style=social)](https://github.com/DongYaoZe/Translate-LADW/network/members)

## 📖 项目简介

本项目是 Sergei Treil 教授的经典教材 **《Linear Algebra Done Wrong》** 的中文翻译版本。

本书是南京大学匡亚明学院线性代数课程（李耀文老师授课）的核心参考书。由于原书为英文，为帮助同学们克服语言障碍、更高效地掌握线性代数的核心思想，我发起了这个翻译项目。

希望这份译稿能成为一份小小的礼物，送给每一位在知识海洋中奋力前行的同学。

**原书信息:**
- **书名:** Linear Algebra Done Wrong
- **作者:** Sergei Treil
- **原书主页:** [https://sites.google.com/a/brown.edu/sergei-treil-homepage/linear-algebra-done-wrong](https://sites.google.com/a/brown.edu/sergei-treil-homepage/linear-algebra-done-wrong)

---

## ✨ 项目特色

- **忠于原文，力求精准**: 在翻译过程中，我们尽最大努力保留原书的精髓，力求译文准确、流畅且易于理解。
- **专业排版**: 全文使用 `LaTeX` 进行专业排版，完美复刻原书中的所有公式和符号，提供与原版媲美的阅读体验。
- **完全免费**: 编译好的 PDF 版本可供任何人免费下载和使用。
- **开源共享**: 所有 `LaTeX` 源码开放，欢迎社区一同参与改进和维护。

---

## 🚀 如何使用

### 1. 直接下载 PDF

您可以直接从本项目的 [Releases](https://github.com/DongYaoZe/Translate-LADW/releases) 页面下载最新编译好的 PDF 文件。

**[>>> 前往下载最新版 PDF <<<](https://github.com/DongYaoZe/Translate-LADW/releases)**

### 2. 自行编译

如果您希望基于源码进行修改或自行编译，请按以下步骤操作：

1.  **克隆仓库:**
    ```bash
    git clone https://github.com/DongYaoZe/Translate-LADW.git
    cd Translate-LADW
    ```

2.  **安装 LaTeX 环境:**
    确保您的系统中已安装了 TeX Live, MacTeX 或 MiKTeX，并支持 `XeLaTeX` 编译。

3.  **编译:**
    使用 `XeLaTeX` 编译器对主文件 `main.tex` 进行编译。通常需要编译两次以上以确保目录和交叉引用正确生成。
    ```bash
    xelatex main.tex
    ```

---

## 🤝 如何贡献

我们非常欢迎并感谢任何形式的贡献！众人拾柴火焰高。

您可以通过以下方式参与本项目：

- **内容纠错**: 如果您在阅读中发现任何错别字、语法错误或翻译不当之处，请毫不犹豫地提交一个 [Issue](https://github.com/DongYaoZe/Translate-LADW/issues)。请在 Issue 中详细说明错误所在章节、页码以及建议的修改。
- **翻译改进**: 对于更复杂的术语或长句，如果您有更好的翻译建议，可以 Fork 本项目，在您的分支上进行修改，然后提交一个 Pull Request。
- **代码与排版**: 如果您对 `LaTeX` 排版有更专业的建议或改进，同样欢迎通过 Pull Request 贡献您的智慧。

---

## ❤️ 致谢

- **Sergei Treil 教授**，感谢他创作了如此优秀的教材。
- **南京大学匡亚明学院李耀文老师**，他的课程是本项目开始的契机。
- **[zhbook](http://haixing-hu.github.io/xelatex-zh-book/) 项目**，本项目使用了其优秀的 `LaTeX` 模板。
- **所有关注、支持和贡献本项目的同学和朋友们**。

---

## 📝 许可协议 (License)

本项目源码采用 [MIT License](https://github.com/DongYaoZe/Translate-LADW/blob/main/LICENSE) 开源。

翻译内容的版权属于原作者 Sergei Treil 和译者。本项目为非营利性质，仅供学习交流使用。严禁用于任何商业目的。

---

## ✉️ 联系方式

如有任何问题或建议，欢迎通过以下方式联系我：

- **GitHub Issues**: [https://github.com/DongYaoZe/Translate-LADW/issues](https://github.com/DongYaoZe/Translate-LADW/issues)
- **邮箱**: `251840159@smail.nju.edu.cn`

---


中文书籍 LaTeX 模板

**注意：** 本模板推荐安装 **texlive** 发行版，并且需要 **XeLaTeX** 编译运行！

```tex
\documentclass[openany,twoside,zihao=-4]{zhbook}
```

本模板为中文书籍 LaTeX 模板，主文件 **main.tex** 给出使用的指南和要求，也展示了论文排版中常用的例子，包括公式、定理、表格、插图、参考文献等。

在线 LaTeX 编辑可以使用 [TeXPage](https://www.texpage.com/)，设置字体 (`fontset=windows`) ，XeLaTeX 编译运行，推荐使用。

中文索引 (默认拼音排序) 使用 zhmakeindex, 参看文件 **索引使用说明.txt**

```latex
% 索引宏包与相关设置
\usepackage[noautomatic]{imakeidx}
\makeindex[columns=2,intoc=true,title={索~~引}]
```

TeX 文件编译顺序:
```bash
xelatex main
bibtex main
makeindex main
zhmakeindex main
xelatex main
xelatex main
```

快速编辑脚本:

makefiles.bat 和 makefiles.sh 包含索引生成的所有编译命令。

makezhindex.bat 和 makezhindex.sh 只包含索引生成的编译命令。

欢迎提出意见或建议。
