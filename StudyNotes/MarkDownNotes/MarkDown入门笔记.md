# MarkDown入门笔记
## 一、MarkDown介绍
Markdown 是一种轻量级的「标记语言」，它的优点很多，目前也被越来越多的写作爱好者，撰稿者广泛使用。看到这里请不要被「标记」、「语言」所迷惑，Markdown 的语法十分简单。常用的标记符号也不超过十个，这种相对于更为复杂的HTML 标记语言来说，Markdown 可谓是十分轻量的，学习成本也不需要太多，且一旦熟悉这种语法规则，会有一劳永逸的效果。

### 1.1 MarkDown介绍
Markdown 是一种用来写作的轻量级「标记语言」，它用简洁的语法代替排版，而不像一般我们用的字处理软件 Word 或 Pages 有大量的排版、字体设置。它使我们专心于码字，用「标记」语法，来代替常见的排版格式。例如此文从内容到格式，甚至插图，键盘就可以通通搞定了。

现在，支持 Markdown 语法的编辑器有很多，包括很多网站（例如 CSDN 博客、CODE CHINA）都支持了 Markdown 格式。Markdown 从写作到完成，导出格式随心所欲，你可以导出 HTML 格式的文件用来网站发布，也可以十分方便的导出 PDF 格式。

### 1.2 使用 Markdown 的优点
- 专注你的文字内容而不是排版样式，安心写作
- 轻松的导出 HTML、PDF 和本身的 .md 文件
- 纯文本内容，兼容所有的文本编辑器与字处理软件
- 随时修改你的文章版本，不必像字处理软件生成若干文件版本导致混乱
- 可读、直观、学习成本低

### 1.3 使用 Markdown 的误区
    We believe that writing is about content, about what you want to say – not about fancy formatting.

    我们坚信写作写的是内容，所思所想，而不是花样格式。

    — Ulysses for Mac

Markdown 旨在简洁、高效，也由于 Markdown 的易读易写，人们用不同的编程语言实现了多个版本的解析器和生成器。这就导致了目前不同的 Markdown 工具集成了不同的功能（基础功能大致相同），例如流程图与时序图，复杂表格与复杂公式的呈现，比如 GFM Markdown 就支持使用 Mermaid 生成图表和流程图。

## 二、段落及强调
在 Markdown 中，段落是由一个以上相连接的行句组成，而一个以上的空行则会切分出不同的段落，一般的段落不需要用空白或换行缩排。

空行的定义是显示上看起来像是空行，便会被视为空行。
比如，若某一行只包含空白 和 tab`` ，则该行也会被视为空行

「一个以上相连接的行句组成」这句话其实暗示了 Markdown 允许段落内的强迫换行，这个特性和其他大部分的 text-to-HTML 格式不一样（包括 MovableType 的「Convert Line Breaks」选项），其它的格式会把每个换行都转成br标签。<br />

这也就意味着在 Markdown 中，如果需要把一段内容当做段落来显示，则需要保证该段内容上方及下方至少各有一个空行
### 2.1 段落的换行
- 如果需要对段落进行换行的话，可以使用两个以上空格加上回车
- 也可以在段落后面使用一个空行来表示重新开始一个段落
- 也可以选择在第一行的末尾添加br标签进行换行 <br> 

### 2.2 强调
Markdown 使用星号 * 和下划线 - 作为标记强调字词的符号。
#### 2.2.1 斜体
在 Markdown 中，将内容用 * 或 _ 包裹起来，包围的字词会被转成用em标签包围，会显示成斜体
*这里是斜体内容1*
_这里是斜体内容2_
<em>这里是斜体内容1</em>
<em>这里是斜体内容2</em>

##### 需要注意的是：
1. 用什么符号开启标签，就要用什么符号结束
2. ** 和 _ 两边都有空白的话，它们就只会被当成普通的符号
3. 如果要在文字前后直接插入普通的星号或下划线，可以用反斜杠\* \_

#### 2.2.2 粗体
用两个 * 或 _ 包起来的话，则会被转成粗体，例如：
**这里是粗体内容1**
__这里是粗体内容2__
<strong>这里是斜体内容1</strong>
<strong>这里是斜体内容2</strong>

#### 2.2.3 删除线
可以使用两个 ~ 来给内容加上删除线，例如：
~~这个内容是被删掉的~~
<del>这个内容是被删掉的</del>

## 三、标题
Markdown 支持两种标题的语法，Setext 和 atx 形式。
### 3.1 Setext 形式标题
Setext 形式是用底线的形式，利用 = （一级标题）和 - （二级标题），例如：

标题1法国海军
=====
标题2
-------
<h1>标题1</h1>
<h2>标题2</h2>
注意，Setext 形式的标题至少需要3个以上的 = 或 _ 才可以正常显示为标题样式。

### 3.2 Atx 形式标题
Atx 形式则是在行首插入 1 到 6 个 #（最多支持 6 级标题） ，对应到标题 1 到 6 级，例如：
#### 标题4
##### 标题5
###### 标题6

## 四、链接
Markdown 支持两种形式的链接语法：行内和参考两种形式。不管是哪一种，链接的文字都是用 [方括号] 来标记。
### 4.1 行内形式链接
行内形式的链接是在方块括号后面接括号并插入网址链接即可，如果你还想要加上链接的 alt 提示文字，只要在网址后面，用双引号把 alt 文字包起来即可，其格式为 [内容](http_url "alt 提示")，例如：

[ CODE CHINA ](https://codechina.csdn.net/)

[ 学习广场 ](https://codechina.csdn.net/courses "CODE CHINA 学习广场")
<p><a href="https://codechina.csdn.net/" target="_blank"> CODE CHINA </a></p>
<p><a href="https://codechina.csdn.net/courses" title="CODE CHINA 学习广场" target="_blank"> 学习广场 </a></p>

### 4.2 参考形式链接
#### 4.2.1 参考链接的引用
1. 参考形式的链接使用另外一个方括号接在链接文字的括号后面，而在第二个方括号里面要填入用以辨识链接的标签：  
[CODE CHINA][1]能够结合云原生技术为 开源技术的教学、学习提供一站式学习、练习的引擎，通过教学培训场景
2. 也可以选择性地在两个方括号中间加上空白：   
[CODE CHINA] [1]能够结合云原生技术为开源技术的教学、学习提供一站式学习、练习的引擎，通过教学培训场景
3. 链接辨识标签可以有字母、数字、空白和标点符号，但是并不区分大小写，比如这两个链接是一样的：  
[link text][a]等同于 [link text][A]
4. 默认的链接标签功能让你可以省略指定链接标签，这种情形下，链接标签和链接文字会视为相同，要用默认链接标签只要在链接文字后面加上一个空的方括号
例如：如果要让 “Google” 链接到 http://google.com/，可以简化成：[Google][]

#### 4.2.2 参考链接的准备
1. 网址定义只有在产生链接的时候用到，并不会直接出现在文档之中。
2. 在文档的任意处，可以把链接标签的链接内容按照格式填写好，其格式为[链接内容格式][id]
3. 链接网址也可以用尖括号包起来
4. 可以把 alt 属性放到下一行，也可以加一些缩排，网址太长的话，这样会比较好看





#### 4.2.3 参考链接的放置
1. 链接的定义可以放在文档中的任何一个地方，建议直接放在链接出现段落的后面，也可以把它放在文档最后面。
2. 使用 Markdown 的参考式链接，可以让文档更像是浏览器最后产生的结果，把一些标记相关的信息移到段落文字之外，这样即使增加链接，Markdown 文档的阅读感也不会被打断。

[id]: http://example.com/ "Optional Title Here"
[1]: https://codechina.csdn.net/courses?utm_source=explore "CODE CHINA 学习广场"
[1]: <https://codechina.csdn.net/courses?utm_source=explore> "CODE CHINA 学习广场"
[1]: https://codechina.csdn.net/courses?utm_source=explore 
    "CODE CHINA 学习广场"
[Google]: http://google.com/
[id]: http://example.com/ "Optional Title Here"

### 4.3 小结
可以使用 [内容](http_url "alt 提示") 的形式添加一个链接
可以使用 参考样式 的方式添加一个链接，其结构为 [内容][1] + [1]: http_url "alt 提示" 的组合

## 五、图片
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内和参考。

### 5.1 行内形式图片
行内形式图片的语法格式为![Alt text](/path/to/img.jpg "Optional title")，比如：
![keyboards](https://source.unsplash.com/500x500/?keyboards "好酷的键盘")

### 5.2 参考形式图片
参考形式图片的语法格式为如下：
![Alt text][id]
[id]: url/to/image  "Optional title attribute"

比如：
![Git 课程][git]

[git]: https://img-blog.csdnimg.cn/20210112151738537.jpg "一张图片"

### 5.3 设置图片大小
到目前为止， Markdown 还没有办法指定图片的宽高，如果需要的话，可以使用普通的 标签。
<img src="https://img-blog.csdnimg.cn/20210112151738537.jpg" width="300px" height="200px" alt="好好学习">

## 六、列表
Markdown 支持有序列表、无序列表和任务列表 三种形式的列表。
### 6.1 无序列表
无序列表使用 * 、 + 或是 - 作为列表标记，比如：
*   香蕉
*   苹果
*   桃子

等同于：
+   香蕉
+   苹果
+   桃子

也等同于：
-   香蕉
-   苹果
-   桃子

### 6.2 有序列表
#### 6.2.1 有序列表语法
有序列表则使用数字接着一个英文句号：
1.  第一天
2.  第二天
3.  第三天
   
当在行首出现 数字-句点-空白 的内容时，Markdown 会将其当做一个列表进行展示，要避免这样的状况，可以在句点前面加上转义符 \ 

#### 6.2.2 可以反义的字符
Markdown 支持在下面这些符号前面加上反斜杠来帮助插入普通的符号：

	\   反斜杠
	`   反引号
	*   星号
	_   底线
	{}  大括号
	[]  方括号
	()  括号
	#   井字号
	+    加号
	-    减号
	.   英文句点
	!   惊叹号

#### 6.2.3 列表也可以进行嵌套或者与其他 Markdown 内容
1. 第一天
	* 起床
	* 吃饭
	* 工作
		- 看邮件
		- 写代码
			// A code block
			打开 CODE CHINA
			![电脑](https://source.unsplash.com/100x100/?computers)
					var x =1000;
            ......	
		- 测试
		- 发布
	* 睡觉
1. 第二天
1. 第三天

### 6.3 任务列表
#### 6.3.1 任务列表语法
任务列表的语法格式为 - [ ] todo，其中带空格的中括号表示未完成的任务，带字母 x 的中括号表示已经完成的任务，比如：
- [x] 起床
- [x] 吃饭
- [ ] 工作
- [ ] 睡觉

#### 6.3.2 任务列表与无序列表或有序列表嵌套使用：
- [x] 起床
- [ ] 吃饭
	- [x] 煮鸡蛋
	- [ ] 烤面包
	- [ ] 热牛奶
1. [X] 工作
	1. [x] 看邮件
	2. [x] 写代码
	3. [ ] 发布
2. [ ] 睡觉

### 6.4 小结
1. 可以使用 * 、 + 或是 - 来创建一个无序列表
2. 可以使用 数字接着一个英文句号 的形式来创建一个有序列表
3. 可以使用 - [ ] todo 的格式来创建一个任务列表
4. 列表之间可以互相嵌套

## 七、分割线及引用
### 7.1 分割线
可以在一行中用三个或以上的*、-、_来创建一个分隔线，行内不能有其他东西。也可以在星号中间插入空白。下面每种写法都可以建立分隔线：
分隔线1
 * * *
分隔线2 
***
分隔线3 
*****
分隔线4 
________
分隔符HTML标签
<hr/>

### 7.2 引用
#### 7.2.1 普通区块引用
Markdown 使用 email 形式的区块引用，我们在要引用内容每行的最前面加上 > ，就可以在 Markdown 文档中创建一个区块引用
> Perl语言的发明人Larry Wall说，好的程序员有3种美德： 懒惰、急躁和傲慢(Laziness, Impatience and hubris)。
> 
> 懒惰，会使得你花大力气去避免消耗过多的精力。它敦促你写出节省体力的程序，同时别人也能利用它们。为此你会写出完善的文档，以免别人问你太多问题。
> 急躁，当你发现计算机懒洋洋地不给出结果。于是你写出更优秀的代码，能尽快真正的解决问题。至少看上去是这样。
> 傲慢，极度的自信，使你有信心写出(或维护)别人挑不出毛病的程序。

#### 7.2.2 段落引用
Markdown 也允许只在整个段落的第一行最前面加上 > 
> Perl语言的发明人Larry Wall说，好的程序员有3种美德： 懒惰、急躁和傲慢(Laziness, Impatience and hubris)。
> 
> 懒惰，会使得你花大力气去避免消耗过多的精力。它敦促你写出节省体力的程序，同时别人也能利用它们。为此你会写出完善的文档，以免别人问你太多问题。
急躁，当你发现计算机懒洋洋地不给出结果。于是你写出更优秀的代码，能尽快真正的解决问题。至少看上去是这样。
傲慢，极度的自信，使你有信心写出(或维护)别人挑不出毛病的程序。

#### 7.2.3 不同级别的区块引用
区块引用可以有级别（例如：引用内的引用），只要根据级别加上不同数量的 > 
> Perl语言的发明人Larry Wall说，好的程序员有3种美德： 懒惰、急躁和傲慢(Laziness, Impatience and hubris)。
>
> > 程序员有三种美德：懒惰，急躁和傲慢。 —— **Larry Wall**
>
> 懒惰，会使得你花大力气去避免消耗过多的精力。它敦促你写出节省体力的程序，同时别人也能利用它们。为此你会写出完善的文档，以免别人问你太多问题。
急躁，当你发现计算机懒洋洋地不给出结果。于是你写出更优秀的代码，能尽快真正的解决问题。至少看上去是这样。
傲慢，极度的自信，使你有信心写出(或维护)别人挑不出毛病的程序。

#### 7.2.4 区块引用内嵌套
引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码块等
> ## 程序员的三种美德
> 
> 1. 懒惰
> 2. 急躁
> 3. 傲慢
> 
> 下面是代码的示例:
> 
>     return shell_exec("echo $input | $markdown_script");

### 7.3 小结
1. 可以在一行中用三个或以上的*、-、_来创建一个分隔线
2. 分隔线行内不能有其他东西，但可以在星号中间插入空白
3. 在要引用内容每行的最前面加上 > ，就可以在 Markdown 文档中创建一个区块引用

## 八、代码块
行内代码的格式很简单，只需要使用两个反引号将代码内容包裹起来即可，比如 `var foo = 'bar';`
### 8.1 缩进显示代码
要在 Markdown 中创建代码块也很简单，只要简单地缩排 4 个空白或是 1 个 tab 就可以，例如，下面的输入：

    This is a code block.
在 Markdown 会转换成：
<pre><code>This is a code block.</code></pre>

这个每行一级的缩排（4 个空白或是 1 个 tab），都会被移除，例如：

    tell application "Foo"
        beep
    end tell
会被转换为：
<pre><code>tell application "Foo"
    beep
end tell</code></pre>

一个代码块会一直持续到没有缩排的那一行（或是文档结尾）。

在代码块里面， & 、 < 和 > 会自动转成 HTML 实体，这样的方式让你非常容易使用 Markdown 插入 HTML 的原始示例代码，例如：
<div class="footer">
    &copy; 2004 Foo Corporation
</div>
会被转换为：
<pre><code>&lt;div class="footer"&gt;
    &amp;copy; 2004 Foo Corporation
&lt;/div&gt;
</code></pre>

### 8.2 高亮显示代码段
除了缩进显示代码段之外，Markdown 还支持高亮显示的代码段，创建高亮显示的代码段时，将代码段由带有三个反引号（ ``` ）的行围起来，并在第一个围栏的末尾标识上语言类型即可，比如：
```javascript
// A highlighted block
var foo = 'bar';
```
也可以不指定语言类型，比如
```
echo "Hello"
```

### 8.3 Diff 语法
此外，Markdown 还支持 Diff 高亮语法，其格式如下
```diff
var foo = 'bar';
+ var x = 200;
* var x = 100;
```

### 8.4 小结
1. 用两个 ` 将代码内容包裹起来就是一个行内代码
2. 缩进 4 个空白或是 1 个 tab 可以创建一个缩进代码块
3. 在代码块的前后各使用三个反引号（ ``` ）把需要高亮显示的代码包裹起来，并在第一个 ``` 的末尾标识上语言类型就可以创建一个高亮代码块

## 九、表格
### 9.1 创建表格语法要求
1. 第一行包含表头，并用"竖线"（ | ）分隔
2. 第二行将标题与单元格分开，并且必须包含三个或更多破折号
3. 第三行以及随后的任何行均包含单元格值
4. 可以通过添加冒号(:)，指定每一列的文本对齐方式，其中：
    - :--: 两端都有冒号表示内容和标题栏居中对齐
    - :--- 左侧冒号表示内容和标题栏居左对齐
    - ---: 右侧冒号表示内容和标题栏居右对齐

### 9.2 注意点
1. 不能在 Markdown 中将单元格分隔成多行，它们必须保持为单行，如果需要，可以使用HTML中br标记对内容进行强制换行
2. 第二行单元长短与标题不需要保持一致，但必须用竖线（|）分隔
3. 可以有空白的单元格

### 9.3 例表如下：

| header 1 | header 2 | header 3 |
| :-----: | :-----: | :----- |
| cell 1 | cell 2 | cell 3 |
| cell 4 | cell 5 is longer |	cell 6 is much longer than the others, but that’s ok. <br> It will eventually wrap the text when the cell is too large for the display size. |
| cell 7 |  | cell 9 |

### 9.4 小结
- 第一行包含表头，并用"竖线"（ | ）分隔
- 第二行将标题与单元格分开，并且必须包含三个或更多破折号
- 第三行以及随后的任何行均包含单元格值
- 不能在 Markdown 中将单元格分隔成多行，它们必须保持为单行，可以使用HTML中br标记对内容进行强制换行
- 可以有空白的单元格

