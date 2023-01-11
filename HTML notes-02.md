# HTML常用标签

## 一. a 标签
### <font color=yellow>1.</font> 作用
&emsp;&emsp;用于从一张页面链接到另一张页面。可以通过它的 <font color=orange>href</font> 属性创建通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接。
```html
<a href=""></a>
```
### <font color=yellow>2.</font> 属性
* href : 包含超链接指向的 URL 或 URL 片段。<br>
  href 的取值:<br>
  * ####  网址 : <br>
    https://google.com <br>
    http://google.com <br>
    //google.com <font color=red>(无协议网址)</font><br>
    ```html
    <a href="https://google.com"></a>
    <a href="http://google.com"></a>
    <a href="//google.com"></a>
    ```
  * 路径 : <br> 
    /a/b/c 以及 a/b/c <br>
    index.html 以及 /index.html
    ```html
    <a href="a/b/c"></a>
    <a href="index.html"></a>
    ```
  * 伪协议 : 
  javascript : 代码 ;<font color=red>(不常用)</font>
  * id : 内部链接
    ```html
    <a href="#XXX">跳转至XXX</a>
    ```
* targe : 指定在何处显示链接的资源。
    * _blank : 在空白窗口打开超链接
    * _top : 在顶层窗口打开超链接
    * _self : 在当前窗口打开超链接
    * _parent : 在父级窗口打开超链接
* download : 指示浏览器下载 URL 而不是导航到它，因此将提示用户将其保存为本地文件。<font color=red>(不常用)</font>
### <font color=yellow>3.</font> a标签的作用
* 用于跳转到外部页面
```html
<a href="https://github.com/Zachariah777/Blog-test/blob/main/HTML%20notes-01.md
">我的博客</a>
```
* 用于跳转到内部锚点
```html
<a href="#XXX">跳转至XXX</a>
```
* 用于跳转到邮箱或电话等
```html
<a href="1792672133@qq.com">我的邮箱</a>

<a href="tel:+86 13812345678">+86 13812345678</a>
```
***
## 二. img 标签
### <font color=yellow>1.</font> 作用
&emsp;&emsp;发出 get 请求,展示一张图片。`<img>` 是空标签，意思是说，它只包含属性，并且没有闭合标签。
要在页面上显示图像，你需要使用源属性（src）。src 指 “source”。源属性的值是图像的 URL 地址。
```html
<img src="" alt="">
```
### <font color=yellow>2.</font> 属性
* alt : 定义了图像的备用文本描述。
* src : 属性是必须的存在的，它包含了你想嵌入的图片的文件路径。
* width : 图像的宽度，在 HTML5 中单位是 CSS 像素。可以省略单位<font color=red>(可以省略单位)</font>
* height : 图像的高度，在 HTML5 中的单位是 CSS 像素。可以只指定 width 和 height 中的一个值，浏览器会根据原始图像进行缩放。<font color=red>(可以省略单位)</font> <br>
## <font color=red>注意 : </font>
* 不可以改变图片长宽比
***
## 三. table 标签
### <font color=yellow>1.</font> 作用
table 标签定义 HTML 表格。
```html
<table>
    <thead>            <!-- 表单头部 -->
      <tr>
        <th></th>
        <th></th>
        <th></th>
      </tr>
    </thead>
    <tbody>            <!-- 表单主体 -->
      <tr>
        <td></td>
        <td></td>
        <td></td>
      </tr>
    </tbody>
    <tfoot>            <!-- 表单尾部 -->
      <tr>
        <td></td>
        <td></td>
        <td></td>
      </tr>
    </tfoot>
</table>
```
### <font color=yellow>2.</font> table 常见样式
* table-layout : 定义了用于布局表格单元格，行和列的算法。
```html
<table table-layout="auto">           <!-- 自动表格布局算法对表格布局。-->
  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>
</table>

<table table-layout="fixed">          <!-- 表格和列的宽度通过表格的宽度来设置 -->
  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>
</table>
```
* border-collapse : 用来决定表格的边框是分开的还是合并的。在分隔模式下，相邻的单元格都拥有独立的边框。在合并模式下，相邻单元格共享边框。
```html
<table border-collapse="collapse">    <!-- 表格中相邻单元格共享边框。 -->
  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>
</table>

<table >                              <!--  HTML 表格的传统模式。相邻单元格都拥有不同的边框。 -->
  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>
</table>
```
* border-spacing : 属性指定相邻单元格边框之间的距离（只适用于 边框分离模式 ）。
```html
<table border-spacing="0">    <!-- 相邻单元格边框之间的距离为 0 -->
  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>
</table>
```
## <font color=red>注意 : </font>
* 不能在 `<table>` 里直接写 `<tr>` 标签
***
## 四. 学习 HTML 心得
&emsp;&emsp;通过对这段时间对 **HTML** 的学习,我了解到 **HTML** 是十分重要的一个超文本标记语言，它里面包含了很多标签，通过这些标签我们就可以根据自己的需求来设计一个网页，并把我们想要表达的内容放进这个网页当中，它定义了网页内容的主体和结构。如果把网页比作是一个完整的人体，**HTML** 相当于骨架， **JavaScript** 相当于肌肉，**CSS** 相当于皮肤，三者结合才能形成一个完善的网页。所以仅仅通过 **HTML** 是不能设计网页的样式的。因此，对于**HTML**的学习要和 **CSS**、**JavaScript** 相互结合，多运用，这样我们才能设计出内容新颖、样式显眼的网页。
