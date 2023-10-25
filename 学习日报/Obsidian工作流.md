<br />

## 扩展配置

> 有以下两款应用的加持搭配第三方依赖，Obsidian 的效率将进一步提升

<br />

### MouseInc

> 自定义专属 Obsidian 的特定手势动作

![](asset/Pasted%20image%2020231025005957.png)

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

#### 外观

- 将大纲视图从右侧移动到左侧，右上方现在主要展示日历，右下方是 MEMOS
	- ![](asset/Pasted%20image%2020231025204035.png)
- 扩展 ben.css 文件


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

#### Template 模板

3. 🌱Record daily，主要用于生成日报，同时在核心插件-日记也进行了配置，用哪个插件都行，后续可以用左侧核心插件-日记进行当天日报的跳转，或者是在 Calendar 插件显示的右侧日历，基于点击的日期跳转到指定日报文件（可以是当天也可以是其他天数，未创建时会询问是否创建）
![](asset/Pasted%20image%2020231024210450.png)

4. 🌳Record weekly，记录周报，通过它能快速生成当周周报模板
![](asset/Pasted%20image%2020231024234748.png)

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


<br />

### templater

> 目前我只用它**识别和展示** <% %> 包裹的变量，完成 dataviewjs 事件

#### Bug

发现 templater 插件和 Obsidian 有时不能实时渲染的问题，提示 templater 解析失败，实际上是因为没有联网的原因，只需要联网后就可以实时渲染了

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

