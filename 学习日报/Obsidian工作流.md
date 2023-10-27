<br />

## 扩展配置

> 有以下两款应用的加持搭配第三方依赖，Obsidian 的效率将进一步提升

<br />

### MouseInc

> 	自定义专属 Obsidian 的特定手势动作

![](asset/Pasted%20image%2020231026155905.png)


### aText

> 智能补全，可以帮我快速实现快捷键等特定功能

![](asset/Pasted%20image%2020231025003952.png)

## Edit

> Obsidian 的配置存储在根目录下的 `.obsidian` 目录中，快速配置另一个仓库的 Obsidian 插件信息的话直接复制粘贴过去即可

<br />

### 双链

#### 文档附件统一存放指定文件夹

![](asset/Pasted%20image%2020231023001901.png)

Wiki 链接普通的 markdown 编辑器（例如 typora）无法识别，同时我们需要将文档中的附件放到一个静态资源文件夹中，因为 Obsidian 无法向 Typora 中一个文档对于一个图片文件夹，所以我们设置一个文件夹对于一个 asset 静态统一存放的文件夹

<br />

### 编辑/预览模式

> Obsidian 不像 typora，实时预览模式目前尚有欠缺
> 
> 引用字段下面的内容多段换行无效，换行加 Tab 无效，需要用 `<br />` 来控制换行
> 
> `<br />` 主要对下行文字有影响，需要换行两次，不然下一行如果是标题将以 markdown 源码的形式展示

#### 外观

- 将大纲视图从右侧移动到左侧，右上方现在主要展示日历，右下方是 MEMOS
	- ![](asset/Pasted%20image%2020231025204035.png)
- 扩展 ben.css 文件
- 打开核心插件：工作区布局管理


<br />

### 快捷键绑定

> `Obsidian` 的快捷键都能在 `设置` 中自定义绑定

<br />

#### 常用快捷键

- `Ctrl+O` ：快速切换文件
- `Ctrl+P` ：打开命令面板
- `Ctrl+E` ：切换编辑/预览模式
- `Ctrl+R` ：使用默认应用打开（这里设置 `Typora` 为默认应用）
- `Ctrl+J` ：打开大纲
- `Alt+C`   ：创建任务（注：需要在每项任务列表中添加任务创建时间才能在周报中展示任务）
- `Ctrl+H` ：查找并替换
- `Ctrl+Shift+I` ：打开控制台
- `Ctrl+,` ：打开设置
- `Ctrl+G` ：打开关系图谱
- `Ctrl+K` ：打开/创建今日日记
- `Ctrl+Shift+L` ：打开文件列表
- `Ctrl+0` ：打开 Tasks 汇集文档
- `Ctrl+M` ：打开当前文档 Mind Map 思维导图

<br />

### Obsidian Git

> 首先需要你当前文件夹已经有 `.git` 文件，与远程仓库进行绑定，`obsidian git` 会根据你所设置的时间间隔当文件内容发生改变时，定时提交并推送到远程，提交的信息由你设定（默认是采用时间变量等上传信息）

![](asset/Pasted%20image%2020231025204647.png)

​	

### Easy Typing

> 简化 Obsidian 中的书写，自动格式化插件自定义文本格式

- 单回车自定义编辑为双回车（**已舍弃**，Obsidian 和 Typora 的设计理念不同，Typora 自带双换行，更方便用户排版，轻量化；Obsidian 则是希望用户对 markdown 进行完美控制，严格按照 markdown 原生单换行进行）
	- ![](asset/Pasted%20image%2020231024164948.png)
- 输入数字、英文、中文之间增加空格
- 当前行首字母大写

#### Bug

- Easy Typing 对 win10 自带的微软拼音不兼容，容易造成输入重复的问题，win11 的微软输入法得以改善，but 我现在是 win10 系统，其他输入法没有此问题，比如正在用的百度输入法
- 百度输入法默认设置中文输入法符号补全，例如（），导致光标调到了（）之后，需要方向键调回，这很不优雅，所以在百度输入法的设置中选择关闭

	

### Various Complements

> 智能补全插件，可以自己设置一个字典 `conf/word.md` 的文件放到插件配置中（例如一些专业名词等），目前前期用不到这个，先禁用

​	

### QuickAdd

#### 问题

- quickadd 的参数变量不清楚有哪些（需网上自行查找，[点击这里](https://momentjs.com/docs/#/displaying/format/)），导致 `Template` 目录下的模板文件并不完美 （**已解决**）
- 由于模板创建文件会导致非 Wiki 链接失效（因为文件地址各不相同，所以有的会打不开），这里还是使用 Wiki 本身本身链接来点击跳转，不过这样的话 Typora 等等其他 markdown 编辑器就看不到文档的附件了（算了，觉得还是不能舍弃，还是放弃 Wiki 专属链接好了）
- 一个设计小缺陷，quickadd 创建新文件时如果涉及变量（例如 `name`、`value`等）创建新文件会在文档中自动打印文件名，通过 tp.file.title 已经可以控制要打印的内容和格式（比如 markdown 给 tp.file.title 加一级标题了），所以对我而言，quickadd 自动打印文件名到文档这一行为是不必要的，但作者又没有设置选项可以控制关闭它😐


![](asset/Pasted%20image%2020231023164103.png)

> QuickAdd 最好用的是 capture 和 template，可通过 `Ctrl+D` 执行文件命令
> 下面介绍我自定义的几种用法：

#### Capture 捕获

1. ✏Capture write，主要用于记录即时灵感或未来要输出的文章标题
![](asset/Pasted%20image%2020231024211222.png)
![](asset/Pasted%20image%2020231024211338.png)
2. 😍Begin write，主要是基于 ✏Capture write 书写待编写的文章
![](asset/Pasted%20image%2020231024233857.png)

3. 🍰Ready to read，主要通过 tasks 收集日报中待看文章标题下的任务列表（通过标签 `#read` 来收集），用于记录自己待看文章和已读文章，待看文章的任务可以散落在各个日报中

![](asset/Pasted%20image%2020231026141047.png)

> capture format ：`[{{value}}](url) -- {{DATE:}} #read`

为什么会有这个待看文章汇总的使用场景？

> 因为之前学前端的时候，观看官方文档，一篇知识点文章往往能牵扯出其他知识点，并且这些知识点都是需要你掌握的，所以待看文章越增越多，导致文章看了好几天，也散落在各个日报中，偶尔会漏看文章，或者我把文章记录到某一篇日报中，而当我关机重启或者关闭该日报所在的 markdown 编辑器再重新打开时，我会不知道待看文章的汇总在哪一篇日报中，需要我一个个去找，这显然是低效率的，而有了 tasks 汇总后我可以随心记录待看文章，因为它会帮我系统的汇总（查询排序的语句是用户（我）自定义的）

> 暂定将待看文章系统的排序整理是在日报中手动整理（缩进，优先级前后，递进关系等等），[read](../Pub/Capture/read.md) 只能起到汇总，如果要整理排序汇总，查询语句可能较复杂（反正我暂时不会也不想学 2023-10-25）

<br />

#### Template 模板

4. 🌱Record daily，主要用于生成日报，同时在核心插件-日记也进行了配置，用哪个插件都行，后续可以用左侧核心插件-日记进行当天日报的跳转，或者是在 Calendar 插件显示的右侧日历，基于点击的日期跳转到指定日报文件（可以是当天也可以是其他天数，未创建时会询问是否创建）
![](asset/Pasted%20image%2020231024210450.png)

5. 🌳Record weekly，记录周报，通过它能快速生成当周周报模板
![](asset/Pasted%20image%2020231024234748.png)

6. 🤔PDF Annotator，基于 Annotator 插件来快速创建 PDF 注释文档模板，使我能编辑记录指定 PDF 的内容和笔记

> Annotator，一款比 Obsidian 自带 PDF 阅读器更强大的注释阅读器（插件），下面有介绍具体介绍 [Annotator](#Annotator)  插件

![](asset/Pasted%20image%2020231027122232.png)

### Tasks

 > 增强版的任务列表，可以快速配置开始时间、截止时间等，搭配 dataview 插件和 Memos 插件使用
 > 
 > 快捷创建任务：`Alt+C`
 > 输入任务内容后单空格能选择各类时间（开始、计划开始、截止时间等）或者触发关键字 `created`、`today`、`monday`等
 > 
> Tasks 的查询管理任务列表查看文件 [Tasks](../Pub/Capture/Tasks.md)（这个很有用，我可以把 tasks 散落在各地，只需要一个文档用 tasks 语法进行汇总就好了，直观清晰， Tasks 还有循环重复的功能，任务完成后在规定时间内可再次生成一个一模一样的 tasks，使用场景比如现实生活中定期发生的事情，发工资或提醒 XX 事情等等）
    Tasks Queries 查询语句，请前往文档 [这里](https://publish.obsidian.md/tasks/Queries/Sorting#Sorting)

在这里补充一点：

[Tasks](../Pub/Capture/Tasks.md) 中已完成标题下的排序除了用 `sort by path reverse` 还可以用 `sort by done`

<br />

### Dataview

> Dataview 可以通过 JS 脚本收集各类数据（例如收集标签、某段时间间隔的所有文档等）进行排序汇总，而 dataviewjs 处理脚本往往涉及变量，需要 templater 插件来识别 <% %> 包裹的变量并进行展示

一定要打开 JavaScript Queries
![](asset/Pasted%20image%2020231025000217.png)

> **讲一下 Tasks 跟 dataview 的区别**
> 
> Tasks 主要是用来汇集各个文档的任务列表部分，dataview 是用来汇集各个文档
> 当然了，Tasks 能做的事情，dataview 也能完成

#### [日记模板](../Pub/Template/日记模板.md)

解释一下 Taskido 中的 forward: true，forward 设置为 true，会把其他任务放到当天显示（点击可定位回去存放该任务的文档中），设置为 false 的话，虽然不在当天日报显示具体内容了，但任务总览里依然会显示 due（已过期） 的数量

日报中的月份刻度显示当前日报位置，需要额外导入 css 文件，第三方导入 css 文件可覆盖 Obsidian 原生 css 样式

![](asset/Pasted%20image%2020231025005136.png)

![](asset/Pasted%20image%2020231025005228.png)

目前我所设置的自定义样式 `ben.css` 只包含对预览/编辑模式-加粗样式的调整，后续会持续更新，代码如下：

```css
/* 更改加粗样式 */

.cm-strong {
  font-weight: bold;
  color: #fff !important;
  background-color: #2ea44f;
  border-radius: 6px;
  line-height: 1.7;
  padding: 2.5px 8px;
  margin: 0px 5px;

}

strong {
  font-weight: bold;
  color: #fff !important;
  background-color: #2ea44f;
  border-radius: 6px;
  line-height: 1.7;
  padding: 2.5px 8px;
  margin: 0px 5px;
}
```

> 下面代码为原作者未完成任务的数据汇集代码，我的日记模板则删除了 hide 的部分

```html
### 未完成任务

```dataviewjs
function callout(text, type) {
    const allText = `> [!${type}]\n` + text;
    const lines = allText.split('\n');
    return lines.join('\n> ') + '\n'
}
const query = `
((created on {{DATE:YYYY-MM-DD}}) AND (done after {{DATE:YYYY-MM-DD}})) OR ((created on {{DATE:YYYY-MM-DD}}) AND (not done))
path includes 学习日报/Day

hide backlink
hide created date
`;
```

#### [周记模板](../Pub/Template/周记模板.md)

> 无论日记模板还是周记模板，使用下面代码收集记录 `未完成任务` 都需要带上创建时间

```dataviewjs
function callout(text, type) {
    const allText = `> [!${type}]\n` + text;
    const lines = allText.split('\n');
    return lines.join('\n> ') + '\n'
}
const query = `
((created on 2023-10-25) AND (done after 2023-10-25)) OR ((created on 2023-10-25) AND (not done))
path includes 学习日报/Day

hide backlink
hide created date
`;

dv.paragraph('```tasks\n' + query + '\n```', 'todo');
```
> 下面代码为原作者 `任务总结` 的数据汇集代码，我的周记模板则删除了 hide 的部分

```txt
## 任务总结

### 本周已完成

```dataviewjs
function callout(text, type) {
    const allText = `> [!${type}]\n` + text;
    const lines = allText.split('\n');
    return lines.join('\n> ') + '\n'
}

const query = `
created (before, after) <% tp.date.weekday("YYYY-MM-DD", 0) %> <% tp.date.weekday("YYYY-MM-DD", 6) %>
done (before, after) <% tp.date.weekday("YYYY-MM-DD", 0) %> <% tp.date.weekday("YYYY-MM-DD", 6) %>
path includes 学习日报/Day
group by created
hide backlink
hide created date
hide due date
hide start date
`;

dv.paragraph('```tasks\n' + query + '\n```', 'done');

--------------------------------------------

### 本周未完成

```dataviewjs
function callout(text, type) {
    const allText = `> [!${type}]\n` + text;
    const lines = allText.split('\n');
    return lines.join('\n> ') + '\n'
}

const query = `
created (before, after) <% tp.date.weekday("YYYY-MM-DD", 0) %> <% tp.date.weekday("YYYY-MM-DD", 6) %>
((done after <% tp.date.weekday("YYYY-MM-DD", 7) %>) OR (not done))

path includes 学习日报/Day
group by created
hide backlink
hide created date
hide due date
hide start date
`;

dv.paragraph('```tasks\n' + query + '\n```', 'todo');
```

#### 阅读书库

> 设想：利用 dataview 汇总 `PDF-Annotate` 的读书笔记文档到 `阅读书库` 目录下创建的 `书评.md` 进行汇总排序

![](asset/Pasted%20image%2020231027145811.png)

> 可以用清单的形式展现，也可以用表格展示更多维度的信息
![](asset/Pasted%20image%2020231027145840.png)

![](asset/Pasted%20image%2020231027145953.png)

![](asset/Pasted%20image%2020231027150009.png)

![](asset/Pasted%20image%2020231027150021.png)


<br />

### templater

> 目前我只用它**识别和展示** <% %> 包裹的变量，完成 dataviewjs 事件
> 
> 但它也可以用来插入指定的文件模板，跟 Obsidian 核心插件 `模板` 是差不多的
> 它可以给指定文件夹绑定指定模板，使用文件夹下创建的文件统一使用统一模板管理，

> [Johnny学OB 第45集 分享OB必用插件Templater的两个懒人用法，看不懂没关系，放到模板下面就可以用\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1RR4y1x7S8/?spm_id_from=333.788.recommend_more_video.-1&vd_source=1f9072e850dde202d6ddd4c60d9d334d)
> 
> 演示代码：[Airtable - Grid view](https://airtable.com/app3mrMDDf1UIQeUB/shrqmxUIfUg8Y0ca8/tblpzHoW1lmd2FSGk)

```txt
1. 将使用当前模板创建的笔记，自动移动到制定文件夹，如果文件没有提前命名,则弹出命名窗口
把这个代码片段放到任何模板的后面，使用时讲“目标文件夹"修改成你想要制定的文件夹

<% await tp.file.move("/目标文件夹/" + ((tp.file.title.includes("未命名") || tp.file.title.toLowerCase().includes("untitled"))  ? (await tp.system.prompt("请输入要创建的文件名")) : tp.file.title)) %>

---

2. 使用Templater新建文件时，自动加上当前所在的文件夹名称

<% await tp.file.rename(tp.file.path(true).split('/')[tp.file.path(true).split('/').length-2] + " " + ((tp.file.title.includes("未命名") || tp.file.title.toLowerCase().includes("untitled")) ? (await tp.system.prompt("请输入要创建的文件名")) : tp.file.title)) %>
```

#### Bug

- 发现 templater 插件和 Obsidian 有时不能实时渲染的问题，提示 templater 解析失败，实际上是因为没有联网的原因，只需要联网后就可以实时渲染了

<br />

### Memos

> 类似 iPhone 的 `提醒`，它可以设置在当天日报的指定标题下同步 `提醒` 的内容
> 目前我暂时打算只当**即时灵感记录和提醒列表**来用，任务列表已经有 `Tasks` 插件了

> 它的优点是集成在工作区界面，可以让我第一时间记录即时灵感，脱离打开指定文件的步骤并节省其时间

<br />

![](asset/Pasted%20image%2020231024164300.png)

有点类似 github 的贴砖记录图，点击 MEMO 😉 能返回首页

![](asset/Pasted%20image%2020231025000350.png)
![](asset/Pasted%20image%2020231025000639.png)

> MEMOS 删除的任务列表在这里→ [delete](Day/delete.md)

<br />

### Calendar

> 一款日历插件，插件默认在右上方展示，点击日期会跳转到该日期对应的日报，如果日报未创建会弹出是否进行创建，一般创建日报对应日期下方会有白点小标志，直观清晰 

![](asset/Pasted%20image%2020231025001002.png)


### Hypothes.is

> 分享 `网页标注` 文章阅读心得，通过浏览器插件 `Hypothesis` 进行网页标注，高亮或注释某一段文章或语句等，并在语句下方进行评论，Obsidian 端下载 Hypothes.is 插件并绑定你的账号 token，设置好同步拉取时间，Obsidian 会定时拉取你在浏览器标注的网页内容和评论到指定文件夹（我指定在 `Pub/Hypo` 目录下，将拉取内容生成文档放到此目录中），然后一般评论我会以任务列表的形式并在任务描述后面加上 `#share` 标签，这样我在 Obsidian 中的 writing 文件设置 tasks 收集带`#share` 标签的任务，可以让我更方便的回顾网页标注的内容、访问原网页和写心得，减少像放到收藏夹吃灰的现象，打通输入（看的信息，例如资讯等）输出（写心得、文章、重新思考的过程）

下面是插件配置格式：

```
{% if is_new_article %}
# {{title}}

## Metadata
{% if author %}- Author: [{{author}}]({{authorUrl}}){% endif %}
- Title: {{title}}
{% if url %}- Reference: {{url}}{% endif %}
- Category: #article
{% endif %}

{%- if is_new_article %}
## Page Notes
{% for highlight in page_notes -%}
{{highlight.annotation}}
{%- if highlight.tags | length %}
Tags: {% for tag in highlight.tags -%} #{{tag | replace(" ", "-")+" "}}{%- endfor %}
{% endif %}
{% endfor %}
{%- endif -%}

{%- if is_new_article -%}
## Highlights
{% for highlight in highlights -%}
- {{highlight.text}} — [Updated on {{highlight.updated}}]({{highlight.incontext}})
{%- if 'Private' != highlight.group %} — Group: #{{highlight.group | replace(" ", "-")}}{% endif %}
{% if highlight.tags | length %}    - Tags: {% for tag in highlight.tags %} #{{tag | replace(" ", "-")+" "}}{% endfor %}
{% endif -%}
{% if highlight.annotation %}   
- Annotation:
{{highlight.annotation}}{% endif %}
{% endfor %}
{% endif %}
```

![](asset/Pasted%20image%2020231025203129.png)

> 当然了，你也可以在命令面板或者左侧栏同步标志手动执行同步

![](asset/Pasted%20image%2020231025203227.png)
![](asset/Pasted%20image%2020231025203749.png)

### [ObWeb](https://github.com/chenyukang/obweb)

> chenyukang 作者研究的一款 Obsidian 移动端同步自动化开源项目，但对我目前来说，关系不大，先跳过

<br />

### Auto Link Title

> 自动插入链接和标题的插件，Obsidian 自带的插入链接不好用，无法识别剪切板内容并粘贴链接，这一插件能直接通过粘贴来插入链接的同时，读取链接的第一级标题，并填充到说明文字中，上面的 ObWeb 标题链接则是通过这一插件来完成的

<br />

### 幻灯片

> Obsidian 自带的核心插件，可以将文档当成幻灯片讲解，通过 `---` 分割每一页幻灯片


<br />

### Automatically Reveal Active File

> Obsidian 的索引有一个小缺陷，就是切换文件的时候（例如 `Ctrl+O`）大纲无法精准定位（虽然 已经 高亮 到新文件了，但无法展示被文件夹隐藏的文件，需要手动打开才能看到，同时如果目标文件超过大纲当前视图区域，也需要你手动去找目标文件，这样很不优雅，`Automatically Reveal Active File` 可以快速定位并高亮目标文件）

#### Bug

>  `Automatically Reveal Active File` 高亮定位插件跟 `Remember cursor position` 保存光标定位插件冲突，根据自身需求，我暂时先选择后者插件

<br />

### Remember cursor position

> 通过保存文档滚动条高度以及光标位置来保存当前文档观看进度，以便切换文件的时候文档不会从头开始，同时文档位置信息保存在本地插件目录中，即使关闭 Obsidian 编辑器，下次打开该文档，依然会跳转到当前观看进度

#### Bug

> 发现一个小 Bug，虽然 `Remember cursor position` 会本地化保存文档进度（也就是关闭编辑器打开仍然是跳转到上一次编辑的进度），但是由于 Obsidian 本身的机制，打开 Obsidian 默认是打开上次编辑文件的位置（估计源代码是默认从头开始展示，因为它自身也没有保存文档观看进度的功能，这是第三方插件集成的功能）
> 
> 所以，你需要 Obsidian 默认打开的是你的目标文档，需要先点击其他文档，再点击回你的目标文档，才能跳转到上次观看进度的位置，这个有点小不方便


<br />

### Better Command Palette

> 增强的命令面板，我暂时不需要


<br />

### Hotkeys for specific files

> 实现为指定文件绑定快捷键打开

![](asset/Pasted%20image%2020231026172003.png)
![](asset/Pasted%20image%2020231026172047.png)

> Tasks 文档是我每天必看的（看看有什么任务没完成），所以在这里添加打开操作的快捷键


<br />

### Excalidraw

> 一个手绘风格的绘画插件
> 
> 新版本更新缺少 `main.js` 文件无法启动，需要去 github 主页的 release 下载

![](asset/Pasted%20image%2020231026181632.png)

![](asset/Pasted%20image%2020231026182054.png)

<br />

### Map Mind

> 根据当前 markdown 的大纲视图生成思维导图的工具
> 
> 自定义快捷打开：`Ctrl+M`

<br />

### Stack tab groups 堆栈选项卡组

> 您可以堆叠选项卡以将其滑动到同一选项卡组中的其他选项卡上。若要堆叠笔记，请选择选项卡组右上角的向下箭头，然后选择 堆叠笔记。

![](asset/Pasted%20image%2020231026232156.png)

<br />

### Day Planner

> 记录日程安排，在侧边栏中会生成纵向时间线，文档顶部还会生成甘特图，当设置时间到来时，它会调用系统自带的通知

![](asset/Pasted%20image%2020231027003442.png)

<br />


### Kanban

> 看板插件能更直观的地管理项目工程，添加卡片、移动卡片、完成卡片、插入图片，同时也能使用双链和其他文档进行联动，例如设置 30 天后的任务，日志面板会在 30 天会有一个任务记录


<br />


### 读书笔记

#深度阅读 #PDF批注 #串联笔记

#### Annotator

> 一款 支持本地和在线的 PDF 以及 Epub 的阅读注释器

##### 语法

```txt
---
annotation-target: 本地附件链接/在线链接
type: pdf/epub
---
```

> 以上语法设置了 `quickadd` 的 template，修改了 Annotator 创建文件时默认用 markdown 形式打开而不是 annotate，只需要再填充 url 然后点击右上角 `···` 的 annotate 打开即可
> 
> **需求**：我希望能在模板中创建一个 url 变量，再 quickadd 创建模板文件的时候，除了自定义名字还能自定义 url 地址，这样的话我就可以直接默认 annotate 模式打开了，减少繁琐步骤
> **解决**：之前以为 value 值只能是标题的值，没想到只需要在模板中设置 `{{VALUE:自定义输入文字}}` 即可创建多个 value 值并在使用 quickadd 创建文件的时候提前自定义好 各个 value 值

^j0cbvb

点击 Annotations 注释还能跳转到标注时的位置并高亮

![](asset/Pasted%20image%2020231027120504.png)

> 在阅读模式下，可以清楚的看到在该附件（PDF）中标注了哪些内容和记下哪些笔记，同时可以双向链接其他文档

![](asset/Pasted%20image%2020231027121257.png)

![](asset/Pasted%20image%2020231027120801.png)

> 小结：Annotator 插件确实也不错，够用，有点是能集成在 Obsidian，便于管理和知识循环。如果你想要一款功能更丰富的 PDF 阅读注释器，我推荐 Xodo APP
> 
> 基于 quickadd 创建的 Annotation template 文件，之后根据考研需要再更改模板文件名的格式和归类

<br />

#### [阅读书库](#阅读书库)

<br />

### 视频笔记

> 如果你想搭建自己的简易媒体库，存放在线视频笔记，下面两款插件是你必不可少的，支持 Bilibili 视频和 YouTube 视频等内嵌到本地 Obsidian 播放

#### 插件支持

- **Media Extended**
- **Media Extended Bilibili**（更新版本，使用 `Media Extend` 本地播放 Bilibili 视频需要搭配 `Media Extended Bilibili`并开启高级功能进行）

> ![](asset/Pasted%20image%2020231027150836.png)

试试在预览模式下，用 Ctrl+鼠标左键点击下面视频链接
[也许是B站最好的Obsidian新手教程！爆肝30天，一站式入门双向链接笔记软件\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV18a411r7mt/?spm_id_from=333.788&vd_source=1f9072e850dde202d6ddd4c60d9d334d)

时间戳
[01:10](https://www.bilibili.com/video/BV18a411r7mt/?spm_id_from=333.788&vd_source=1f9072e850dde202d6ddd4c60d9d334d#t=70.260965)

![](asset/Pasted%20image%2020231027152758.png)

> 注：打上时间戳后，不能在实时预览模式中用 ctrl+左键打开视频，会直接弹出网页
> 只能在预览模式下才生效

![](asset/Pasted%20image%2020231027153310.png)
#### B 站投稿案例实例

![](asset/Pasted%20image%2020231027153047.png)

![](asset/Pasted%20image%2020231027153056.png)


<br />

#### 数据复盘

![](asset/Pasted%20image%2020231027153454.png)

##### Charts

> 通过 `ctrl+p` 打开命令面板输入 Charts 即可创建图标，输入参数信息，一份精美数据图标即创建成功

```chart
type: bar
labels: [Firday]
series:
  - title: test1
    data: [1]
  - title: test2
    data: [5]
  - title: test3
    data: [-3]
tension: 0.2
width: 80%
labelColors: false
fill: false
beginAtZero: false
bestFit: false
bestFitTitle: undefined
bestFitNumber: 0
```

也可以通过快捷键绑定的方式

![](asset/Pasted%20image%2020231027153825.png)

![](asset/Pasted%20image%2020231027153956.png)

![](asset/Pasted%20image%2020231027154033.png)

<br />

### Obsidian 插件开发

> 教学链接：[程序员高效使用 Obsidian -- 插件开发\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1rL4y1F7h5/?spm_id_from=333.788&vd_source=1f9072e850dde202d6ddd4c60d9d334d)
> 
> 即使不开发也可以了解一下，可以帮助更全面了解 Obsidian，像下面的 `main.js` 是 `main.ts` 通过 `npm run build` 打包编译而来的入口文件
> - **mainifest.json** 记录 Obsidian 元数据
> - **main.js** 记录所有处理逻辑
> - **style.css** 是样式文件

![](asset/Pasted%20image%2020231026185254.png)

如果遇到插件（重启还）打不开的情况，可以进入控制台查看 error 报错

![](asset/Pasted%20image%2020231026185310.png)

#### Obsidian42 - BRAT

> 当你的插件没有发布时，可以通过 `brat` 插件分享 BETA 版本的插件仓库地址给你指定的人内测

<br />

#### 开发相关资料

![](asset/Pasted%20image%2020231026190439.png)

![](asset/Pasted%20image%2020231026190548.png)

![](asset/Pasted%20image%2020231026190637.png)


### obsidian to anki

> 背诵卡片
> 
> 实用性 `obsidian to anki` 和 `Spaced Repetition` 待测试

<br />

### Spaced Repetition

> 也是背诵卡片
> 
> [无需 Anki 直接在 Obsidian 里面背卡片 | 笔记神器 Obsidian 完全指南\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1ho4y127nW/?spm_id_from=333.999.0.0&vd_source=1f9072e850dde202d6ddd4c60d9d334d)

<br />


### Obsidian 仓库多端同步

<br />


### Copy Block Link

> 快速复制块链接，提升操作体验
> [几招教你提高 Obsidian 中块引用的操作体验 - 知乎](https://zhuanlan.zhihu.com/p/411484717)
---
> 相信有不少从 Roam 转移到 Obsidian 的用户会特别怀念它的 Ctrl+Shift+C 来复制当前行的块引用字符串，或者怀念它支持右键直接复制当前的块链接，而 Obsidian 中却刚好有这样一个插件支持了几乎一模一样的操作。
> 
> 这就是由 Kanban 插件的作者开发的一款微型插件（下载链接：[obsidian-copy-block-link](https://link.zhihu.com/?target=https%3A//github.com/mgmeyers/obsidian-copy-block-link)），虽然他开发过很多其它的微型插件，但是这款应该是我最为喜欢的插件。
> 
> 你在当前段直接右键点击就会有熟悉的 Copy Block Link 以及 Copy Embed Link 两个选项，如下图所示：
> 
> 这里分别有内嵌型和引用型
> ![](asset/Pasted%20image%2020231027171713.png)
> 
> 点击 Copy Block Link 就可以将当前块的链接复制到粘贴板，然后你就可以去到你想要粘贴的地方进行粘贴了。而 Copy Embed Link 也类似，粘贴出来的会是块嵌入效果。
> ![](asset/Pasted%20image%2020231027171725.png)

