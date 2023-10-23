## Edit

> Obsidian 的配置存储在根目录下的 `.obsidian` 目录中，快速配置另一个仓库的 Obsidian 插件信息的话直接复制粘贴过去即可

	

### 双链

#### 文档附件统一存放指定文件夹

![](asset/Pasted%20image%2020231023001901.png)

Wiki链接普通的markdown编辑器（例如typora）无法识别，同时我们需要将文档中的附件放到一个静态资源文件夹中，因为Obsidian无法向Typora中一个文档对于一个图片文件夹，所以我们设置一个文件夹对于一个asset静态统一存放的文件夹

	

### 编辑/预览模式

> Obsidian 不像 typora，实时预览模式目前尚有欠缺

	

### 快捷键绑定

> `Obsidian` 的快捷键都能在 `设置` 中自定义绑定

#### 常用快捷键

- `Ctrl+O` ：快速切换文件
- `Ctrl+P` ：打开命令面板
- `Ctrl+E` ：切换编辑/预览模式
- `Ctrl+R` ：使用默认应用打开

	

### Obsidian Git

> 首先需要你当前文件夹已经有 `.git` 文件，与远程仓库进行绑定，`obsidian git` 会根据你所设置的时间间隔当文件内容发生改变时，定时提交并推送到远程，提交的信息由你设定（默认是采用时间变量等上传信息）

​	

### Easy Typing

> 简化 Obsidian 中的书写，自动格式化插件自定义文本格式

- 单回车自定义编辑为双回车
- 输入数字、英文、中文之间增加空格
- 当前行首字母大写

	

### Various Complements

> 智能补全插件，可以自己设置一个 `conf/word.md` 的文件放到插件配置中（例如一些专业名词等），目前前期用不到这个，先禁用

​	

### QuickAdd

[writing](Pub/Capture/writing.md)