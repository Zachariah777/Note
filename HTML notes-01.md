# HTML 入门笔记

## 1. HTML 是谁发明的?
&emsp;&emsp;[HTML](https://zh.wikipedia.org/wiki/HTML) 的英文全称是 Hyper Text Markup Language，即超文本标记语言。HTML是由Web的发明者 Tim Berners-Lee(李爵士)和同事 Daniel W. Connolly于1990年创立的一种标记语言，它是标准通用化标记语言SGML的应用。

## 2.  HTML 起手应该怎么写?
   ```html
<!DOCTYPE html>
<html lang="en">                                              <!-- 文档类型,中文应改成"zh-CN" -->
   <head>
      <meta charset="UTF-8">                                     <!-- 文件字符编码,建议默认 -->
      <meta http-equiv="X-UA-Compatible" content="IE=edge">      <!-- 告诉IE采用最新内核版本去渲染网页 -->
      <meta name="viewport" content="width=device-width, initial-scale=1.0">    <!-- 禁用页面缩放 -->
      <title>Document</title>                                    <!-- 网页标题 -->
   </head>
   <body>
   </body>
</html>
 ```

## 3. 常用的表章节的标签有
#### 1. h1~h2: 标题标签, 六个不同的级别的标题，h1 级别最高，而 h6 级别最低。
```html
<h1>一级标题</h1>
…
<h6>六级标题</h6>
```
#### 2. section: 章节标签, 标签定义文档中的章节、页眉、页脚或文档中的其他部分.
```html
<section>
   <h1>标题</h1>
   <p>内容</p>
</section>
```
#### 3. article: 定义文章
```html
<article>
  <h1>标题</h1>
   <p>内容</p>
</article>
```
#### 4. p: 段落标签, 表示文本的一个段落.
```html
<p>内容</p>
```
#### 5. header: 头部标签, 用于展示介绍性内容.
```html
<header>头部内容</header>
```
#### 6. footer: 尾部标签, 表示最近一个章节内容或者元素的页脚。
```html
<footer>尾部内容</footer>
```
#### 7. main: 规定文档的 body 或应用的主体部分。
```html
<main>
   <p>内容</p>
</main>
```
#### 8. div: 通用型的流内容容器,是块级元素.
```html
<div>
   <h1>标题</h1>
   <p>内容</p>
</div>
```

## 4. 全局属性有
* class: 规定元素的一个或多个类名
* contenteditable: 规定元素内容是否可编辑。
* hidden: 表示一个元素尚未或者不再相关,可用于隐藏内容.
* id: 定义了一个全文档唯一的标识符,该属性不会报错,所以尽量用class替代使用.
* style: 规定元素的行内 CSS 样式。
* tabindex: 规定元素的 tab 键次序。
* title: 规定有关元素的额外信息。

## 5. 内容标签有
#### 1. ol>li: 有序列表,此标签指定列表中的条目是有序排列的
```html
<div>
   <ol>
      <li>内容1</li>
      <li>内容2</li>
      <li>内容3</li>
   </ol>
</div>
```
#### 2. ul>li: 无序列表,此标签指定列表中的条目是无序排列的
```html
<div>
   <ul>
      <li>内容</li>
      <li>内容</li>
      <li>内容</li>
   </ul>
</div>
```
#### 3. dl>dt+dd: 描述列表,是一个包含术语定义以及描述的列表
```html
<div>
   <dl>
      <dt>列表标题</dt>
      <dd>列表内容</dd>
      <dd>列表内容</dd>
      <dd>列表内容</dd>
   </dl>
</div>
```
#### 4. pre: 表示预定义格式文本。在该元素中的空白符（比如空格和换行符）都会显示出来。
#### 5. code: 用于呈现一段计算机代码. 默认情况下, 它以浏览器的默认等宽字体显示.
#### 6. hr: 水平分割线,表示段落级元素之间的主题转换.
#### 7. br: 换行标签,表示段落级元素之间的主题转换.
#### 8. a: 超链接标签,用于通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接的标签。
```html
<div>
   <a href="#">链接标题</a>
</div>
```
#### 9. em: 斜体标签, 标记出需要用户着重阅读的内容.
#### 10. strong: 加粗标签, 表示文本内容十分重要，用粗体显示。
#### 11. quote: 内链引用标签, 表示一个封闭的并且是短的行内引用的文本.
#### 12. blockquote: 块级引用标签, 代表其中的文字是引用内容。