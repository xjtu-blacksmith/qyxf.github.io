---
date: 2019-10-04
author: '`能动少C71尤佳睿`'
---

# 学研部排版学习路线

本页面提供给**钱院学辅学研部**的成员，提供一条基本的**排版**知识学习路线与简短的介绍。

这篇教程的内容将包括：

1. Markdown 的简介、教程推荐与编辑工具；
2. LaTeX 公式的基本语法，以及在 Markdown 中使用 LaTeX 公式；
3. 使用 Markdown 排版的规范标准（钱院学辅中文排版规范）。

## 1 Markdown：最高效的文档格式

### 1.1 关于 Markdown
Markdown 是一种文本标记语言，即在纯文本（`txt` 文件）的基础上引入了一些**标记**，使得其中的内容可以呈现出特殊属性——例如，产生标题、加粗字、列表与链接的分野。从这个意义上来说，可以将 Markdown 理解为一种「文档格式」，就像大家常用的 Word 文档一样。只不过，Markdown 一方面是**文本文件**，可以用任何文本编辑器（如记事本）打开、编辑，Word 文档（**二进制文件**）必须用专门的软件打开处理；另一方面，Markdown 能实现的「功能」比 Word 要少很多，但恰可满足 99% 文档的需要，同时极大地节省了编写、处理、储存与发布的时间，因此可谓为「最高效的文档格式」。

> 尽管 Markdown 文档本身不需要用专门软件打开，但要想让 Markdown 中的标题能「显示」为标题，需要用可视化的文本编辑器**预览**，或利用一些小工具将其**转换**为 PDF、HTML 等可以看见样式的文档格式。

这篇文章即是用 Markdown 撰写，读者可以感受到：Markdown 提供的功能，已经足够强大。

### 1.2 如何撰写 Markdown 文档
Markdown 的学习非常简单。如果将其视为一种「编程语言」，则可以毫不犹豫地说：Markdown 是世界上「最简单」的编程语言。

网络上 Markdown 的教程不计其数（但误导人的也不少），读者可以任选一篇阅读。这里，我们推荐以下的几份：

- [Markdown 入门教程](https://mazhuang.org/2018/09/06/markdown-intro/)（From 码志）
- [Markdown 语法说明](https://www.markdownguide.org)（英文，涵盖了大多数 Markdown 方言的基本语法与拓展语法）
- [Markdown 语法说明](https://www.markdown.cn)（以上的中文翻译版本）
- [超简明语法表格](https://commonmark.org/help/)（英文，CommonMark 语法，相当于绝大多数 Markdown 的「基本语法」）
- [实践学习 Markdown](https://www.markdowntutorial.com)（英文，答题过关的模式）

下面一份 Markdown 代码，基本上概括了所有 Markdown 的基本语法。

```markdown
# 一级标题

## 二级标题

### 三级标题

这也是一级标题
------

及二级标题，你可以根据喜好选用
======

这是一段普通的文本，可以**加粗**，可以用*斜体*——但中文的「斜体」不
推荐使用。

> 你也可以用这种方式，创建引用段落——它们不一定用来「引用」。

[超链接](https://qyxf.site/)与
![图片](https://qyxf.site/assets/images/favicon-16x16.png)
的写法是类似的，只不过后者外加一个感叹号而已。

---

上面的就是分割线（代码叫 `hr`），尽量在上下都留出空格（否则可能被认
成一级标题或普通段落）。

- 这是一个列表项
+ 这也可以是一个列表项
    * 这则是一个子列表项
    - 这也是一个子列表项
- 但最好还是统一用一种符号


- 与上面相较

- 这个列表在生成时

- 会有更宽的行距


## 常见错误（用数字列表列出）

1. 引用、列表、分割线等特殊内容与上下文之间不留出空格，这样很可能生
成出错。
2. 标题的 `#` 号与标题内容要留出一个空格，否则在很多编译器上会有问题。
3. 段落与段落之间要空一整行（更多也可），单纯换行顶多是一个空格。
4. 勿像 Word 中一样连续打几个空格：连续的空格会被转换成单个，因为你
不需要那么多。段首空格会被忽略。

```

以下仅补充几个教程中很少涉及、强调的概念，提请读者注意：

**「样式与内容分离」**. Markdown 是文本标记语言，仅指明一份文档中有标题、引言、脚注、强调文本等若干特殊格式的文本，但并没有告诉编译器或编辑器：标题应该多大？引言是否应用一个矩形包围起来、居中？强调文本可否用另一种颜色或另一种字体？事实上，「标题」、「引言」等这些说法，代表的是文档的「内容」或「内容格式」；而它们用多大的字、是否居中等，属于「样式」。Markdown 强调「内容与样式分离」，只指定了内容的格式，样式则**完全**交由编辑器、编译器等处理 Markdown 的程序来实现。因此，大家在撰写 Markdown 文档时，应注意这一原则，不要关心——更不要试图**调整**文档的样式。

> 如果你对文档最终的呈现样式有特殊要求，或对样式设计者的成果有所不满，请直接与他们取得联系、陈述你的要求，或使用自己设计的「样式表」（通常用 CSS 格式实现）。

**关于 Markdown 方言.** Markdown 刚出现时，由一份用 Perl 语言编写的脚本实现。其作者 John Gruber 为此撰写了一篇[语法说明](https://daringfireball.net/projects/markdown/syntax)，不幸的是：这份说明既未涵盖可能出现歧义的特殊情况，甚至也和其脚本中的具体实现有所出入。此外，他本人秉持「自由」的哲学，拒绝对 Markdown 的语法与实现方式（即如何将 Markdown 文档无歧义地生成与编译）做具体规定，这导致此后各种「Markdown 方言」层出不穷，它们一方面各自支持许多拓展功能（如表格、自动链接、代码高亮），另一方面对具体的 Markdown 段落可能有不同的解释方法。尽管已经有像 [CommonMark](https://commonmark.org) 这样试图实现「标准化」的行动，但 Markdown 方言四分五裂的格局已难以扭转。读者在使用不同的编辑、编译器时，应尽量查明其采用的 Markdown 语法细则（可查找他们提供的语法文档或 Markdown 教程）；否则，应谨慎使用各种拓展特性，包括：

- 表格语法（大多数编译器已支持）
- 自动链接
- 脚注（GitHub 等网站不支持）
- 删除线（采用一对 `~~` 围成）
- HTML 的标签（部分标签可能不支持）
- LaTeX 公式（编写时可以采用，排版人员将最终实现它们，但请作者调好自己的编辑器以支持公式预览）

**文档的撰写方式.** 采用了 Markdown 这样一种高效方式，你就应当学会改掉一些在 Word 中养成的陋习，包括：

- **不要**在段落的开头用好几个空格实现「首行缩进」——首行缩进本来是一种样式，你不需要操心。在 Markdown 中，段首的空格会被忽略。
- **不要**用加粗、调样式代替标题：请多使用标题语法，并合理安排标题层级（从最高级开始连续布置，不要超过三级，或跳级使用）。各级标题是最终生成目录、书签、协调样式的唯一凭据。
- **不要**继续依靠网上建议的 `<br/>` 标签手动换行：习惯用段落组织文本，换行往往会破坏文章的连续性。
- **不要**在正文中任意用空格、<kbd>Tab</kbd> 键缩进：不当的缩进可能造成识别错误（例如，四格缩进将把文本转换成代码块）。Markdown 不是脚本、代码，不必用缩进来体现内容的层次——这是标题的任务。

### 1.3 Markdown 编辑工具
常用的**通用编辑器**——如最流行的 [VS Code](https://code.visualstudio.com)、[Atom](https://atom.io)、[Sublime Text 3](https://www.sublimetext.com)——等，都可以通过**插件**很好的支持 Markdown，相关方法可在网上轻松找到。除此以外，更推荐初学者使用的是 Markdown 的**专用编辑器**，它们往往能带来更好的体验。包括：

- [Typora](https://www.typora.io/) 界面清新优雅，功能强大，通用性强；各个桌面系统均支持（OS X 系统的版本最新），可设置界面为中文
- [Haroopad](http://pad.haroopress.com/user.html) 界面简洁明快，功能异常强大，适合开发者使用；各个桌面系统均支持，可设置界面为中文（此软件由韩国的团队开发）
- [MarkPad](http://code52.org/DownmarkerWPF/) 界面传统规整，通用性较强；仅支持 Windows 10 系统
- [iA Writer](https://ia.net/zh-hans/writer) 界面极其简明，没有多余样式，专注于优雅、高效的写作，适合撰写文学作品、公众文章；支持 Windows、OS X、Android 和 iOS 系统。

由于 Markdown 本身十分容易，这些软件的上手并不困难。你可以在这些软件中精心调配各个部分的样式表，改变设定以提高写作速度与体验。

在本地编辑器之外，网页编辑器、笔记软件（支持同步）与博客网站也是可行的选择。常用的笔记软件中，[印象笔记](https://www.yinxiang.com)、[有道云笔记](https://note.youdao.com)、[为知笔记](https://www.wiz.cn/zh-cn)等均已很好的支持 Markdown；网页端中，[简书](https://www.jianshu.com)可能是国内比较流行的方式。在网络端撰写，可以很快的将内容公之于众，便于分享、传播。

## 2 LaTeX 公式
原则上，针对学辅的资料编写工作而言，Markdown 所提供的「有限」功能已经绰绰有余，足以让我们编写出高质量、有内涵的作品。然而，有一项功能，Markdown 自身并不支持——数学公式与符号的编排、显示。

在 Markdown 中，数学公式必须引入外部的插件来实现。一般，我们采用 **LaTeX 公式语法** 来撰写公式的内容，而利用 MathJax 引擎将公式代码转换为真正的符号与式子。

> LaTeX（正规的排版方式应该为 $$\mathrm{\LaTeX}$$）是一种文档排版代码/引擎，负责一整个文档的内容与排版。详细内容，可以参考[学辅技术讲座](/technique/technical-lecture)中的相关内容。这里仅涉及其中的**公式功能**，原因是：LaTeX 的整个系统以难学、难用著称，但 LaTeX 公式系统却被广泛使用，几乎成为各种文档环境中公式排版的第一或唯一方式。
>
> 换句话说：LaTeX 难学，没有需求时可先搁置一旁；但 LaTeX 的公式，却值得现在就花一点时间「速成」。

### 2.1 命令与环境
在编排公式时，先应几个来自于 LaTeX 的基本概念：

1. **命令**：有如一般编程语言中的「函数」，以反斜杠 `\` 开头，后接一串字母；整个命令直到一个非字母的字符截止。许多命令后往往还需要附带**参数**，它们通常会用一对花括号 `{}` 包围。
2. **环境**：有如一般编程语言中的「函数体」或「语句体」，通常由一对命令 `\begin{xxx}` 与 `\end{xxx}` 包围起来，其中 `xxx` 就是这个环境的名称。除此之外，一些特殊的字符也应被视为环境的**定界符**，例如由一对美元号 `$...$` 括起来的内容也是一个环境。
3. **字符**：LaTeX 对于不同的字符有非常详尽的处理方法，在公式的代码中一般有这样几类字符：
    - 特殊字符：如命令开头的反斜杠 `\`、标识环境的 `$`，以及 `_`、`^`、`&` 等。它们有特殊的功能，不会以它们本身的样子显示在最终的公式中。
    - 定界符：主要是花括号 `{}` 和环境命令 `\begin{xxx}...\end{xxx}`，它们决定了不同命令生效的范围，同样不会以本身的样子显示在最终的公式中。
    - 空白字符（如空格与换行）：在 LaTeX 公式中，一般字符间的空白字符不会显示在最终的公式中。
    - 一般字符：除了以上几类之外的其他字符，它们会原样显示在公式中（样式、位置、尺寸等则会有差异）。

例如，我们来看下面的一段 LaTeX 公式代码：

```latex
$ I(x) = \int_a^b f(x) \mathrm{d} x $
```

其最终将生成公式 $$I(x) = \int_a^b f(x) \mathrm{d} x$$。依照上面所提的几条基本概念，我们对这一串看似复杂的代码进行拆解：

- 代码中共出现了两个反斜杠 `\`，因此其中共计两个命令，分别是 `\int` 与 `\mathrm`，后者还紧跟着一个用花括号包围的参数 `d`。其实，`\int` 是积分（**int**egral）号命令，能够生成一个积分号（$$\int$$）；`\mathrm` 则是数学正体（**math**ematical **r**o**m**an style）命令，将其后的字符 $$d$$ 从公式默认的斜体（italic style）改为正体（$$\mathrm{d}$$）。
- 整个公式为一对美元号所包围，说明其被正常地包裹在「数学环境」之中。否则，代码将不会被渲染为公式。
- 除开确定环境的 `$` 符号，公式中还出现了两个特殊字符 `_` 与 `^`，它们分别表示「下标」与上标，并附属于之前的积分号命令 `\int`。`_` 号紧跟的字符 `a` 成为了积分号的下标（下限），而 `^` 号紧跟的字符 `b` 成为了积分号的上标（上限）。另外，如果你希望生成 $$\int_{12}^{24}$$ 这样上标与下标不止一个字符的公式，则应在 `_` 或 `^` 后将参数用花括号包起来：`\int_{12}^{24}`。
- 除开以上分析的特殊字符，其余的字符都将原样展示在公式中——正如我们所看到的那样。代码中的空格被忽略掉，渲染引擎会帮我们留出合适的间隙——在一般情况下。

### 2.2 常用命令与环境
LaTeX 公式排版的难点有二：

1. 如何确定用哪一类命令、环境排版公式；
2. 这些命令和环境怎么写（具体的名称、参数表等比较难记）。

这些问题会难住一些初学者，但读者应记住：只要花一段时间熟悉常见的命令与环境，并努力锻练打字能力，公式的排版将变得异常轻松。下面简单介绍一些最常用的命令、环境，之后会提供一些可供查阅的完整表格。

#### 2.2.1 符号命令分类

公式中所需要的命令，无非两种：特殊数学符号（占绝大多数，如之前的 `\int`）、个别的样式调整（像之前的 `\mathrm` 一样）。前者又可进一步举例细分为如下几类：

- **希腊字母**：出现频率很高。你只需要记得这些希腊字母的**英文拼法**就行，例如 `\alpha` 将显示为 $$\alpha$$，而 `\Gamma` 将生成 $$\Gamma$$。你可以在百度百科的[对应页面](https://baike.baidu.com/item/希腊字母)中查找不同希腊字母的「字母名称」，这就是紧跟在 `\` 后的命令名。（一些情景下已经支持直接输入 Unicode 希腊字符，例如在这个页面上的 `$α$` 代码可直接生成 $$α$$。）

- **加减乘除**：如果你的键盘上有，你可以直接打出；注意我们常用的乘号 $$\times$$ 应该用命令 `\times`，而除号 $$\div$$ 用命令 `\div`（divide）敲出（这两个符号在大学中是不常用的）。

- **点号**：一般可用垂直居中的 `\cdot`（$$\cdot$$，center dot）表示。如果需要将它们连成三个表示省略，则可以用 `\cdots`（$$\cdots$$） 与 `\ldots`（$$\ldots$$，lower dots），后者靠在下方。垂直三点 $$\vdots$$ 为 `\vdots`（vertical dots），对角线排列的三点 $$\ddots$$ 为 `\ddots`（diagonal dots）。

- **比较符号**：等号、大于号、小于号可直接打出，大于等于（greater or equivalent）可用 `\geq`（$$\geq$$）或 `\geqslant`（$$\geqslant$$，slant 表示一横的倾斜）两种风格，小于等于（less or equivalent）号类似：`\leq` 或 `\leqslant`。不等于号为 `\neq`（$$\neq$$）。近似可用 `\sim`（$$\sim$$，similar）或 `\approx`（$$\approx$$，approximate）等符号表示。

- **集合关系**：常用的有被包含 `\subset`（$$\subset$$，subset 表「子集」）与包含 `\supset`（$$\subset$$，super set 表「超集」）、真子集 `\nsubseteq`（$$\nsubseteq$$，not equivalent subset），属于 `\in`（$$\in$$）和不属于 `\notin`（$$\notin$$）、并 `\cup`（$$\cup$$，cup 表「杯子」形容了此符号的形状）、交 `\cap`（$$\cap$$，cap 表「帽子」，与前者恰好方向相反）。

- **「大符号」**：往往指那些纵向尺度较大、常有上下标的符号，包括积分号 `\int`（$$\int$$）、求和号 `\sum`（$$\sum$$）、连乘号 `\prod`（$$\prod$$，production）、集族并集号 `\bigcup`（$$\bigcup$$，与 `\cup` 的区别是它较大且可以有上下标）、集族交集号 `\bigcap`（$$\bigcap$$）等。

- **定界符**：通俗来说就是各种「括号」。圆括号、方括号可以直接用对应键打出。花括号 `{}` 被用于包藏参数、确定命令的作用范围，因此其不会显示在公式之中；如果要将其打出，则应使用 `\{` 与 `\}`，这里的反斜杠起到了「转义」的作用（像在很多编程语言中一样）。其他可用的还有：绝对值界 `|` 可直接打出；范数界 `\|`（$$\|$$，其效果好于直接打两条竖线 `||`）；尖括号 `\langle` 与 `\rangle`（$$\langle$$ 与 $$\rangle$$，left angle 与 right angle）、上取整 `\lceil` 与 `\rceil`（$$\lceil$$ 与 $$\rceil$$，ceil 即「天花板」）、下取整 `\lfloor` 与 `\rfloor`（$$\lfloor$$ 与 $$\rfloor$$，floor 即「地板」）。

- **算子**：一般是用若干字母排列而成的函数名称，例如三角函数（`\sin`、`\cos`、`\tan`）、指数对数函数（`\exp`、`\log`、`\ln`）、最大值 `\max` 与最小值 `\min`、极限 `\lim` 等等。它们的共同特点是：命令中的字符，会以数学正体的形式显示出来，如 `\sin` 将显示为 $$\sin$$。它们都支持上下标。

- **带参命令**：即**必须**指定参数的命令，最常用的包括：
    - 分数（fraction）命令 `\frac{a+b}{c+d}` 生成 $$\frac{a+b}{c+d}$$，其中第一个参数为分子，第二个参数为分母。
    - 组合数（binominal number，二项式系数）命令 `\binom{a+b}{c+d}` 生成 $$\binom{a+b}{c+d}$$，结构与分数类似。
    - 根式（square root，平方根——但此命令不限于平方根）命令：`\sqrt[n]{x}` 生成 $$\sqrt[n]{x}$$，第一个用方括号包围的是次数（可以省略，此时表示平方根），第二个参数为被开根的内容。

几乎所有的符号命令，都可以归入以上的几个类别之中。读者如果能熟记以上所提到的这些符号，则可以在不查表的情况下应付 90% 的符号了。至于像无穷大号 `\infty`（$$\infty$$，infinity）等这种常用而不能归类的孤例，读者除了记住之外，也可以时常查阅以下给出的一些「符号表」

> 这类表格大多数情况下没有用，少数情况下你要用——但找不到想要的符号。~~所以，百度、Google 等搜索引擎无疑是最大赢家、幕后黑手。~~

- [The Comprehensive LaTeX Symbol List](/BookHub/001.resources/symbols-a4.pdf)：包含了整个 LaTeX 系统中的特殊符号，数学符号仅为其一子集；所有需要的符号一定在这里，但你需要事先翻阅，弄清其复杂的结构.
- [LaTeX Mathematical Symbols](/BookHub/001.resources/latex-math-symbols.pdf)：仅涉及常用的符号，基本够用。内容丰富。
- [Codecogs 公式编辑器](https://www.codecogs.com/latex/eqneditor.php)：一个在线编辑器，提供若干按钮，便于你通过图形化的页面找到所需的符号。境外网站，加载速度可能较慢。

#### 2.2.2 样式调整命令
另一类命令是样式调整命令。

**字体样式调整命令**. 使用这些命令时，必须用花括号将待调整的内容包围——哪怕只有一个字符。

- `\mathrm` 可能是最常用的一个，因为我们经常需要在默认为斜体的公式中插入正体字符（对单位、下标、自定义算子等）。不过，更推荐使用的是 `\text`；这个命令的机制并非单纯调整样式，但可以视为与 `\mathrm` 等价的命令，且比其更好用。

- 要打出表示数集的 $$\mathbb{R}$$、$$\mathbb{C}$$ 等镂空粗体（blackboard bold）字符，应使用 `\mathbb` 命令。

- 一般的粗体（bold font shape），可以用 `\mathbf` 命令打出，只不过该命令对字母和数字以外的字符无效。如有需要，可以尝试 `\boldsymbol` 与 `\bm` 等命令。

- 其他的特殊字体还有花体（calligraphical） `\mathcal` 与文本体（script） `\mathscr` 等，它们都在数学中常用，表示较高级别的范畴（如集族、映射族等等）。

> 以上这些命令，不一定在所有情况下都能使用。在 LaTeX 中，这涉及到宏包的问题；在其他场合下，则取决于所用的渲染工具是否支持相应的命令。

**定界符调整命令**. 定界符的大小一般是固定的，这时我们可能会碰到这样的情况：输入代码

```latex
$ f(x) = ( \frac{a^x}{b} ) $
```

将得到

$$ f(x) = ( \frac{a^x}{b} ) $$

很显然这里的括号太小了。为此，我们可以用一些命令来调整定界符的大小。精细的做法是采用不同等级的调整命令，例如

```latex
$ f(x) = \Bigl( \frac{a^x}{b} \Bigr) $
```

这里用一对命令 `\Bigl` 与 `\Bigr` 吸附在左右括号之前，调整了其大小。就像下面这样，令人满意。

$$ f(x) = \Bigl( \frac{a^x}{b} \Bigr) $$

这样的命令有很多，依次排成一个级别序列：`\big`、`\bigg`、`Big`、`\Bigg` 等。如果你对此不感兴趣，则可以在各种情况下都使用自动调整的 `\left` 与 `\right` 命令：

```latex
$ f(x) = \left( \frac{a^x}{b} \right) $
```

这一对通用命令可以在大部分情况下解决你的问题，但有时会产生偏差。

#### 2.2.3 数学环境
所有命令都必须在**数学环境**之中才能被渲染为公式。一般而言，有两大类环境：

1. 行内环境（inline）：顾名思义，指那些出现在文本行内的短小公式或符号。例如这里的公式 $$a+b=c$$ 便由行内数学环境所容纳。
2. 行间环境（block 或 displayed）：较大的公式，从段落中分离出来独占一行，居中显示。例如以下的

$$I(x) = \int_a^bf(x)\mathrm{d}x$$

（你可以比较这个公式跟第一个例子的显示效果有何差别。）

行内环境与行间环境的使用，取决于具体需要。下面给出了一些行内与行间环境的例子；此处不再絮叨这些环境的具体用法，但给出相应的链接供读者查看。

环境特性|命令或定界符|参考或备注
---|---|---
行内环境|`$...$` 或 `\(...\)`|最简单的一种
行间环境，不标号|`$$ ... $$` 或 `\[\]`|不能换行
行间环境，标号|`\begin{equation} ... \end{equation}`|不能换行
行间可换行，标号，不对齐|`\begin{gather} ... \end{gather}`|[此博文](https://liam.page/2014/09/08/latex-introduction/)的「8.8.2. 公式组」
行间可换行，标号，对齐|`\begin{align} ... \end{align}`|[此博文](https://liam.page/2014/09/08/latex-introduction/)的「8.8.2. 公式组」
行间内嵌对齐环境|`\begin{aligned} ... \end{aligned}`|必须嵌在已有的行间环境内；参考[此博文](https://liam.page/2014/09/08/latex-introduction/)的「8.8.1.2. 对齐」
行间内嵌条件环境（左侧自带一花括号）|`\begin{cases} ... \end{cases}`|必须嵌在已有的行间环境内；参考[此博文](https://liam.page/2014/09/08/latex-introduction/)的「8.8.3. 分段函数」

> 一般的，在某一数学环境中，如果可能的话，`&` 将表示「从此处开始与上下对齐」，而 `\\` 将表示「在此处换行」。

以上这些公式环境，都是针对在 LaTeX 系统之外使用 LaTeX 公式而言的。部分引擎可能不支持以上的一些写法，或要求所有环境都要包在某一类定界符（如一对 `$`）下，请读者留意。

#### 2.2.4 矩阵
矩阵是一类特殊的内嵌数学环境。通用的写法是

```latex
\begin{matrix}
a & b & c\\
d & e & f
\end{matrix}
```

注意这里的 `matrix` 环境要放在一个行间环境中。以上命令将生成

$$\begin{matrix}
a & b & c\\
d & e & f
\end{matrix}$$

通常当我们使用矩阵时，都需要指定一个定界符。固然，我们可以用 `matrix` 环境外加两侧的自动定界符 `\left` 与 `\right` 等实现，但这过于繁琐。简要的方法是使用一些预定义、自带定界符的环境，包括：

- 自带圆括号 $$()$$ 的 `pmatrix` 环境；
- 自带方括号 $$[]$$ 的 `bmatrix` 环境；
- 自带花括号 $$\{\}$$ 的 `Bmatrix` 环境；
- 自带绝对值界的 `vmatrix` 环境与自带范数界的 `Vmatrix` 。

只需要将上面的 `matrix` 替换即可。此外，若要在行间打印小矩阵（如 $$\left(\begin{smallmatrix}a&b\\c&d\end{smallmatrix}\right)$$，则可使用 `smallmatrix` 环境（定界符必须自己添加）。

#### 2.2.5 上下标
上下标是除开特殊符号外最常用的一类操作，无处不在。在第一个公式样例中，我们已经说明：

- `_` 符号后紧跟一个字符（或用一对 `{}` 包起来的若干内容），将为其之前的命令或符号添加对应下标；
- `^` 与之机制类似，不过生成的是上标。

一般而言，这样两类对象会经常用到下标：

- 单个字符（$$2^3$$、$$x_i$$）、定界符 -- 包括矩阵的定界符（$$\|\mathbf{x}\|_2$$、$$\left(\begin{smallmatrix}a&b\\c&d\end{smallmatrix}\right)^\mathrm{T}$$）；

- 「大符号」（$$\sum\limits_{k=0}^N$$）、算子（$$\max\limits_{x\in X}p(x)$$）。

这里分为两类的依据是：前者的上下标通常在主体符号的斜上方、斜下方，而后者的上下标通常在主体的正上方、正下方（「大符号」中的积分号除外，大多数人倾向于用侧旁的上下标）。这些符号在配置上下标时，通常会有一个默认设置，该设置与符号本身、所处环境类别（行内或行间）都有关，例如默认的行间求和号用的却是斜侧上下标：$$\sum_{k=0}^N$$，并不雅观。

你可以在主体符号后紧跟一个 `\limits` 命令（不要放在别的位置），使上下标切换至正上方、正下方；反之，紧跟一个 `\nolimits` 命令，将使它们切换至侧旁位置。

> `\limits` 可以理解为：按照极限号通常的写法（$$\lim\limits_{x\to\infty}$$）来组织上下标。

### 2.3 用「拆解法」处理公式
在掌握各种公式、环境之后，编写公式就已经是小 case 了，几乎不需要再做练习。以下提供一种名为「拆解法」的思路，供读者参考；它代表了排版一个公式时的一般思路，可以无障碍的复制到其他情形之下。

例如，考虑以下一个公式，它来自于对流体力学中 Navier-Stokes 基本方程的研究：

$$ \begin{aligned}
& \iint_{ \mathbb{R}^3 \times (0, +\infty) }\left\{ - \sum_{i=1}^3 u_i \frac{\partial \theta_i}{\partial t} - \sum_{i,j=1}^3 u_i u_j \left( \frac{\partial \theta_i}{\partial x_j}\right) \right\} \mathrm{d}x \mathrm{d}t \\
= & \iint_{ \mathbb{R}^3 \times (0, +\infty) }\left\{ \nu \sum_{i,j=1}^3 \left( \frac{\partial^2}{\partial x_j^2} \theta_i \right) u_i + \left( \sum_{i=1}^3 \frac{\partial \theta_i}{\partial x_i} \right) p \right\} \mathrm{d}x \mathrm{d}t
\end{aligned} $$

让我们依次来拆解这个公式，确定其代码。

1. **环境**：易见这是一个行间公式，并且有一个对齐的换行（对齐了二重积分号 `\iint`）。所以应该采用这样的环境包围公式：
    ```latex
    $$ \begin{aligned}
    & \\
    &
    \end{aligned} $$
    ```
    即行间公式嵌入对齐子环境。

2. **层级结构**：细数第一行（第二行类似）的定界符，发现最多只有两层：一组花括号包裹一组圆括号，并伴有一些求和号。由于定界符内有分数结构 `\partial`，故需用 `\left` 与 `\right` 命令调整定界符大小。在花括号外，左侧有一个双重积分号 `\iint`，右侧有两个微元 `\mathrm{d}x`、`\mathrm{d}t`。那么，可以初步写出两公式的层级结构：
    ```latex
    $$ \begin{aligned}
      & \iint \left\{ - \sum \frac{}{} - \sum \left( \frac{}{} \right) \right\} \mathrm{d}x \mathrm{d}t \\
    = & \iint \left\{ \sum \left( \frac{}{} \right) +\left( \sum \frac{}{} \right) \right\} \mathrm{d}x \mathrm{d}t
    \end{aligned} $$
    ```

3. **填入符号**：除开定界符、「大符号」之外，还有一些必要的普通符号。依次填入，并同时补上所有的上下标——在 LaTeX 中，上下标「顺水推舟」地附属于之前的符号，不需要专门规划其结构。
    ```latex
    $$ \begin{aligned}
      & \iint_{ \mathbb{R} \times (0, +\infty) } \left\{ - \sum_{i=1}^3 u_i \frac{\partial \theta_i}{\partial t} - \sum_{i,j=1}^3 u_i u_j\left( \frac{\partial \theta_i}{\partial x_j} \right) \right\} \mathrm{d}x \mathrm{d}t \\
    = & \iint_{ \mathbb{R} \times (0, +\infty) } \left\{ \nu \sum_{i,j=1}^3 \left( \frac{\partial^2}{\partial x_j^2} \theta_i \right) u_i +\left( \sum_{i=1}^3 \frac{\partial \theta_i}{\partial x_i} p \right) \right\} \mathrm{d}x \mathrm{d}t
    \end{aligned} $$
    ```
    由此即完成了公式的编写。这里的各个符号命令（如偏微分算子 `\partial`、各个希腊字母、二重积分号 `\iint`），都属于最常用的命令，读者应该在浏览过几次命令表格后将它们熟记。

以上这种分层拆解的方法，有利于初学者快速弄清一个复杂公式的代码结构，以尽可能少的错误、重复工作来完成公式的编写。待读者技术熟练之后，则不需要再这样从外至内的分层编写，而可以~~用一种「大江东去浪涛尽」的宏伟气势~~从头写到尾，中间基本上不会碰到什么问题——除了括号未配对、拼写错误、少打个别字符等。

> 在编写技术相对熟练之后，一种提高效率的手段是：压缩空格与大括号的数量（如上面一段代码中的空格大多可以去掉）。具体细节在此不详述，读者可以自行尝试——当然，提高效率的同时，会影响之后对公式代码的复查。

### 2.4 MathJax 引擎的使用
在 LaTeX 系统之外的地方（例如本页面上），如何渲染 LaTeX 公式代码呢？在种种其他的应用场景之中，网页（包括 Markdown 文档）是最为重要的一个，因此网页端的 LaTeX 渲染最值得我们关注。

早先，仿照着已经大获成功的 HTML、XML 等文档格式标准，万维网联盟（W3C）指定了「数学标记语言」**MathML**。其「条理清晰、逻辑严密」，只可惜格式过于复杂，难以自行撰写。例如，对于二次方程的求根公式：

$$ x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

我们知道 LaTeX 代码中只需一小段代码就能解决，而 MathML 却需要这样实现：

```xml
<math mode="display" xmlns="http://www.w3.org/1998/Math/MathML">
  <mrow>
    <mi>x</mi>
    <mo>=</mo>
    <mfrac>
      <mrow>
        <mo form="prefix">&#x2212;<!-- − --></mo>
        <mi>b</mi>
        <mo>&#x00B1;<!-- &PlusMinus; --></mo>
        <msqrt>
          <msup>
            <mi>b</mi>
            <mn>2</mn>
          </msup>
          <mo>&#x2212;<!-- − --></mo>
          <mn>4</mn>
          <mo>&#x2062;<!-- &InvisibleTimes; --></mo>
          <mi>a</mi>
          <mo>&#x2062;<!-- &InvisibleTimes; --></mo>
          <mi>c</mi>
        </msqrt>
      </mrow>
      <mrow>
        <mn>2</mn>
        <mo>&#x2062;<!-- &InvisibleTimes; --></mo>
        <mi>a</mi>
      </mrow>
    </mfrac>
  </mrow>
  <annotation encoding="TeX">
     x=\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
  </annotation>
  <annotation encoding="StarMath 5.0">
     x={-b plusminus sqrt {b^2 - 4 ac}} over {2 a}
  </annotation>
</math>
```

换句话说：这种格式是给机器看的，不是给人看、给人用的。它实现了很多额外功能，例如加入了 (La)TeX、StarMath 等公式系统中的对应代码，但我们对此并不感兴趣。

鉴于 W3C 对于 XML 格式的这种执念，许多替代方案衍生出来，目前最通行的便是由美国数学学会（AMS，早先他们也曾对 LaTeX 的公式系统做出过巨大贡献）维护的 **MathJax** 引擎。与标记语言 MathML 不同，MathJax 并不打算重新设计公式的编码，而是直接将页面上的 LaTeX 公式代码渲染成可以显示在网页上的**公式对象**。

在网页上引入 MathJax 的脚本、配置之后，其将自动执行「翻译」LaTeX 代码的功能，无需再多操心。目前，大多数 Markdown 编译器都采用 MathJax 引擎渲染公式。

总之，对于读者而言，只需记住：**在支持 MathJax 的系统下，可以像在 LaTeX 系统中一样输入公式，没有太大差别。**

> 在个别情况下，MathJax 可能只能识别特定类型的数学环境。例如，本网页开发时所用的 Jekyll，配置了名为 Kramdown 的 Markdown 编译引擎，在其下只能识别用双美元号 `$$ ... $$` 包围的公式（但其可以自动判断公式是行内还是行间环境）。详见本网站项目的[技术文档](https://github.com/qyxf/qyxf.github.io/wiki)。

## 3 资料的组织与排版规范

资料的内容很重要，但呈现的方式甚至更为重要。具体而言，这里所谓的「方式」应归结为两个层面：内容的组织结构，以及排版方式。

### 3.1 资料的组织结构

如果你正在编写一份资料，内容甚多，则你应该好好考虑资料的组织形式。例如，对同样一本书，这样的目录结构是较为清晰的：

> - 第一章 实数域与数列极限
>     + 1.1 实数集的构造
>         * 1.1.1 自然数集：Peano 公理
>         * 1.1.2 整数集的构造
>         * 1.1.3 有理数集的构造与性质
>         * 1.1.4 实数集构造：分割方法
>         * 1.1.5 实数集构造：完备数列方法
>     + 1.2 实数公理体系
>         * 1.2.1 Dedekind 公理与连续性公理
>         * 1.2.2 确界定理与区间套定理
>         * ...
>     + 1.3 数列及其极限
>         * ...
>     + ...
> - 第二章 函数极限理论
>     + ...
> - 第三章 连续函数理论
> - 第四章 一元微分学
> - ...

相反地，以下这种目录则显然会使人「望而却步」：

> - 1 实数集的构造
>     + 1-1 自然数集
>     + 1-2 Peano 公理
> - 2 整数集与有理数集的构造
> - 3 实数集构造：分割方法
>     + 3-1 另一种方法：完备数列方法
>     + 3-2 实数公理体系简述
>         * 3-2-1 第一类公理
>             - 3-2-1-1 第一类公理的特征
>             - ...
> - 4 Dedekind 公理
>     + 4-2 补充：连续性公理
> - ...

作为资料的编写者，你应该在编写资料之前事先规划各部分内容的层次（以目录作为一个指导标准）。通常而言，这样几种做法值得推荐：

**「挂靠」已有章节**. 编写某些课程的辅导资料时，可以直接依靠课程、课本的章节划分组织内容。这是最常见的一种做法；在此情况下，二级标题基本已经够用，不需要再向下划分太多的层次。

**简单分类**. 对于特定内容而编写的资料，可以简单分几类，将它们作为资料的一级标题。例如，要从以上例子所涉及的数学知识中抽取「实数公理体系简述」为主题，编写一本小册子。那么，可以根据这些公理（总计 7 -- 9 个）的一些特征，将其分为两类或三类，分别分析；再加上「两类公理的联系与区别」、「绪论」、「总结」等循规蹈矩的内容，一份言简意赅、层次清晰的资料就已经初步浮现了。

**三级标题系统**. 这是一般情况下适用的原则，包括：

+ 标题不要超过三层，不要跨级（例如，一级标题下直接附属三级标题——这在 Markdown 文档中常常出现）。
+ 各层上的内容范畴大致同级。
+ 每一部分的专属内容（例如，一个二级标题的专属内容指：在某一二级标题下方，而没有归属于任何一个三级标题的内容）不要太多，且尽量平衡。
+ 最低级标题的总数可稍多些，但更高级的标题尽可能少。
+ 相近的内容应合并，泛化的概念应放在高级标题之下。

> 以上所言的「一级标题」，不是指作品的名称、总标题，而是指目录下的第一级标题——通常所言的「章」。

以上这些原则，「玄之又玄」，十分抽象。只有以一个普通读者的身份反复品味、分析自己的作品，并适当征求他人的看法，你才能在内容的组织能力上有所进步。

### 3.2 Markdown 文档排版规范
在总体的组织结构之外，文档内部的种种细节也应非常注意。在互联网上，一些资料不仅「长得漂亮」（样式精巧），内容也很赏心悦目；一些资料虽然没有华丽的外表，却给人一种清新、整洁的感受——例如这个[博客](https://yihui.name)中的页面。后者所依靠的，就是排版上的精雕细琢。

作为资料的编写者，我们并不刻意追求排版的高质量；但是，我们应对资料的阅读者具有起码的尊重，不应拿模糊的公式截图来困扰读者，也不应该用随机分布的行间距、字间距、单词拼写和字体切换来降低读者的阅读效率。

为了提高学辅资料的排版质量，此处呼吁学研部的每一位资料编写者在工作过程中，尽力遵守以下几条基本的排版原则：

<tb-cap>钱院学辅中文排版规范（第一版，2019 年 8 月 10日）</tb-cap>

原则内容|示例
---|---
请使用直角引号。|✔ 「这样」，「这样地『这样』」。<br>✘ “这样”，“这样地‘这样’”。
中文字符与西文、数字之间必须留有空格。|✔ 我们学校的名称是 Xi'an Jiaotong University 或西安交通大学，创建于 1896 年。<br>✘ 我们学校的名称是Xi'an Jiaotong University或西安交通大学，创建于1896年。
中文半角符号与西文之间不留空格。|✔ 西安交通大学，英文名为 Xi'an Jiaotong University，是一所坐落在西安市（Xi'an）的综合性大学。<br>✘ 西安交通大学，英文名为 Xi'an Jiaotong University ，是一所坐落在西安市（ Xi'an ）的综合性大学。
除非是纯西文的短语、句子、段落、文档，均采用中文的标点符号（Markdown 所需的标记符号当然除外）。|✔ Notes：普通话（Mandarin）是一种非常棒的语言，真的！<br>✘ Notes: 普通话 (Mandarin) 是一种非常棒的语言, 真的!<br>✔ 你可以参见《Legendary: Guides to Mandarin & Cantonese》。<br>✘ 你可以参见《Legendary：Guides to Mandarin＆Cantonese》。
在遵守以上原则的前提下，链接文本与其他文本之间不留空格。|✔ 你可以参考[开源中国](https://www.oschina.net/)或 [GitHub 首页](https://github.com/)给出的说明。<br>✘ 你可以参考 [开源中国](https://www.oschina.net/) 或[GitHub 首页](https://github.com/)给出的说明。
在遵守以上原则的前提下，对于带字母单位的数字，值与单位之间不留空格。|✔ 今天的天气为「中雨」，最高气温为 26℃，城区降水量可达 15mm 以上。<br>✘ 今天的天气为「中雨」，最高气温为 26 ℃，城区降水量可达 15 mm 以上。

> **对以上内容的补充说明**：
>
> - 关于第一条引号的用法，需要强调的是：选择直角引号而非横排引号，并非由于谁优谁劣，而是想推动你在学研部的工作中尝试一种新的方式。你可能需要参考：[知乎 - 如何输入直角引号（「」和『』 ）？](https://www.zhihu.com/question/19755746)
> - 关于空格，需要注意的是：在 LaTeX、Word 等排版系统中，中文与英文、半角数字之间的间距往往能够自动生成。编写者应根据资料的**最终形式**决定是否需要手动加空格。

在没有出现新的问题之前，这份规范将维持现状。
