



<div style="font: 26pt 方正小标宋GBK;text-align: center;white-space:pre-line">
我的工具链
</div>



<span class="summary-keyword-title" style="font: 12pt SimHei;">摘  要：</span>工具链

<span class="summary-keyword-title" style="font: 12pt SimHei;">关键词：</span>CSS；实验报告；前端开发；Typora



## 总体思路

本实验希望使同学们摆脱书写实验报告时调整格式的痛苦，从而使大家能更多集中于实验报告内容和质量，而不是耗费大量时间于格式调整。

#### 目的一：减轻同学写作负担

在Word中自定义样式是比较复杂的操作。作为计算机专业文档中往往会出现大量代码，在Word中不好排版。Markdown中则可以很容易的插入代码块、行内代码块与公式、行内公式，还可以用Typora进行编辑、转换为Word文档或pdf文件。Markdown的文件格式也容易用Sublime Text、VSCode等编辑器打开编辑，可被git等代码管理软件以行为单位记录变动。

#### 目的二：进行CSS练习

CSS是层叠样式表 (Cascading Style Sheets)的简写，是前端开发的必修课；除了大一下学期的网页设计制作外我并没有接触CSS知识，也没有编写CSS代码的经验，所以希望通过这个项目使自己得到锻炼。

### 实验意义

其实我想不出来实验意义，但报告格式上要这么写，我就只能这么写。

## 实验设计

### Mardown简介

Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。


Markdown具有一系列衍生版本，用于扩展Markdown的功能（如表格、脚注、内嵌HTML等等），这些功能原初的Markdown尚不具备，它们能让Markdown转换成更多的格式，例如$\rm\LaTeX$，Docbook。Markdown增强版中比较有名的有Markdown Extra、MultiMarkdown、 Maruku等。这些衍生版本要么基于工具，如Pandoc；要么基于网站，如GitHub和Wikipedia，在语法上基本兼容，但在一些语法和渲染效果上有改动。


Markdown的语法简洁明了、学习容易，而且功能比纯文本更强，因此有很多人用它写博客。世界上最流行的博客平台WordPress和大型CMS如Joomla、Drupal都能很好的支持Markdown。完全采用Markdown编辑器的博客平台有Ghost和Typecho。

Markdown经常用于编写软件说明文档，并且以“README.md”的文件名保存在软件的目录下。


### Typora简介

Typora 是一款支持实时预览的 Markdown 文本编辑器。它有 OS X、Windows、Linux 三个平台的版本，并且由于仍在测试中，是完全免费的。

Typora的特色在于“所见即所得”，拥有类似Word的编辑方式，新用户很容易习惯和上手。

Typora是高度可定制化的，支持直接输入html代码和用CSS自定义主题。

#### Typora自定义主题简介

Typora做的主要工作就是把Markdown标记转换为HTML标记再渲染出来，比如`**强调**`就会被转换成`<strong>强调</strong>`。

<div class="table-caption">部分Markdown语法与HTML标记对照</div>
| Markdown语法    | HTML标记 |
| :-------------- | :------: |
| \*\*strong\*\*  |  strong  |
| \*em\*          |    em    |
| \`inline-code\` |   code   |
| !\[\](img-src)  |   img    |

所以Typora的编辑界面本质上就是一个浏览器，你甚至可以按<kbd>Ctrl</kbd>+<kbd>F12</kbd>来呼出浏览器的开发者工具。Typora允许自定义CSS样式，同时给出了标记转换的规范和主题编写教程，这样只要对照《武汉大学计算机学院本科生课程设计报告书写印制规范》（下简称“规范”）编写出对应的CSS代码就能够在Typora界面呈现出符合要求的样式，达到用Markdown写实验报告的目的。

#### 方案局限

在编写主题的过程中，我们遇到了很多困难，有的是能够克服或者绕过，或者通过某些工具能够达到的，比如一篇实验报告除了标题和正文，还有封面、摘要、声明、教师评价等成分，并不能由Markdown标记表达，还好Typora支持直接书写HTML代码。但是Typora的即时渲染策略是忽略`div`标记中的`class`和`id`属性，所以并不能在编辑时呈现上述成分的字体效果，只能把样式代码手动添加到相应元素的`style`属性中。

更多问题是当前无法克服的。通过CSS样式能够实现标题和图表的自动编号，但是规范示例中“参考文献”和“附录”是不带编号的，即使在正文里能使用一个前置div标记使其取消编号，在目录中却无法取消。

Typora通过Markdown标记`![]()`只生成`img`标记，而图标题和图序号需要`figure`标记，只能手动输入HTML标记来插入图片。自动生成的图序号中的“图”字也是粗体，和示例中“图”字为普通字重也不符合。所以我们提供了不进行自动编号的主题。

有些特性必须借助Prince软件才能解决，比如页面的页眉和页脚编号。由于Typora生成HTML文件时对我们写的CSS代码会有所修改，以及Typora生成的HTML代码不满足某些要求，在把导出的HTML文件提供给Prince前我们还需要用一个Python脚本处理一下。

Typora的表格是不带标题（caption）的，如果需要则需自己写带`caption`标签的HTML代码，或者在表前写`<div class="table-caption">表标题内容</div>`，前文所述脚本将会把它转换成表的标题。

## 实验成果



## 参考文献



## 附图附件



## 备        注



























