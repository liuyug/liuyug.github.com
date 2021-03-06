---
layout: default
title: 您应当避免的 12 个 HTML 标签错误
---
您应当避免的 12 个 HTML 标签错误
================================

:Date: 2012-10-3
:Category: WEB
:Tags: html

From: `12 Evil HTML Tag Mistakes You Really Should Avoid <http://smashinghub.com/12-evil-html-tag-mistakes-you-really-should-avoid.htm>`_.

在 WEB 页面访问中，人们经常遇到 HTML 代码编写错误，开发者应当真正的认真考虑并小心使用 HTML 标签。下面讨论了 12 个常见的易忽略的错误，这些提示将会有助于 HTML 开发者。

1. HTML 标签嵌套错误
--------------------
.. image:: images/highlighting_tag_tree1.png 

![alt text](images/highlighting_tag_tree1.png)

关闭 HTML 标签十分重要。标签的开启与关闭要一一对应，而且顺序相反。新手往往不在意标签的关闭。校验 HTML 代码时会发现错误，并且 Style 样式也不能正确提交。一定要小心这个错误。

错误用法::

    <div><p><a>This is my Smashing text</p></div></a>

正确用法::

    <div><p><a>This is my Smashing text</a></p></div>

2. 不正确的使用 List
--------------------
.. figure:: images/HTML_Lists1.png 

OL 和 UL 标签总是被用于显示多个项目，并以不同的方式使用。List 标签在显示大量信息时特别有用，它能避免使用大量的换行符( <br /> )，搜索引擎也能识别 List 标签，使用标准的 HTML 标签会比 <br /> 做得更好。

3. 不正确的使用 Form 标签
-------------------------
form 和 table 标签常常使人迷惑。是应当先用 table，还是先用 form，请看下面:

错误用法::

    <table><form><tr><td>..... </td></tr></form></table>

正确用法::

    <form><table><tr>.... </tr></table></form>

4. 在 inline 元素中使用 block 元素
----------------------------------
.. figure:: images/inline-block.gif

HTML 开发者都知道元素总是以 inline 或 block 的方式显示，每一个元素缺省被创建在 inline 或 block 元素内。在文档中，首先是 block 元素，如 <p> 和 <div> 等，inline 元素则在 block 元素内。整个文档由若干个这种结构体组成。因此，要确保 inline 元素放在 block 元素内，而不是其他地方。

block 元素::

    <div>, <h1>…<h6>, <p>, <ul>, <ol>, <dl>, <table>, <blockquote>, <form> 

inline 元素::

    <span>, <a>, <strong>, <em>, <img />, <abbr>, <acronym>

5. 缺少 alt 属性
----------------
当使用图像并显示在主页时，一定要使用 alt 属性。这是非常必要的，用户可以决定是否显示图像，特别是在一个慢速连接或小屏幕时。这个属性能描述所显示的图像。不要使用 ``alt="image"`` 或 ``alt=""`` ，这没有任何益处。

错误用法::

    <img src="smiley.gif" alt="" />

正确用法::

    <img src="smiley.gif" alt="Smiley face" width="42" height="42" />

6. 粗体和斜体的使用方法错误
---------------------------
一般 ``<b>`` 用于粗体， ``<i>`` 用于斜体，但这两种表示方法只是计算机语法，用 CSS 样式来表达会更好一些。如果文本必须使用粗体或斜体，那么使用 ``<strong>`` 和 ``<em>`` ，他们与 ``<b>`` 和 ``<i>`` 的功能一样，但看上去更好。

7. 不必要的换行
---------------
在一段中，使用标签 ``<br />`` 来换行。但是许多人在两个元素间加入换行，这是不对的。只有在必要时，才用 ``<br />`` 切换到下一行。

错误用法::

    This is my first paragraph
    <br />
    <br />
    <br />
    
    This will be my test description

正确用法::

    <p>This is my first paragraph</p>
    <p>This will be my test description</p>

8. 不正确的使用删除线
---------------------
.. figure:: images/strikethrough1.jpg

``<strike>`` 和 ``<s>`` 曾用于修正 WEB 中的文本，但是现在，他们已经废除了。新的标签是 ``<ins>`` 和 ``<del>`` 。他们用于 WEB 页和文档中的插入和删除。

9. 在 HTML 代码中使用 CSS 样式
------------------------------
你应当听说过许多次，在 HTML 代码中使用 CSS 样式不是个好注意，你知道为什么吗？这是因为 CSS 样式和 HTML 代码是完全分离的，他们共同组成结构化文档。在 HTML 代码中直接使用样式是不正确的。这就是为什么总是建议在样式表中表达样式。

错误用法::

    <p style="font-size: 14px;font-weight: bol">

10. 包含和去除边框
------------------
边框属性是一个表示效果，因此它只应当被 CSS 样式修改。不要担心默认的边框样式。

错误用法::

    <img src="smiley.gif" alt="" border="0" />

11. 忽略 <h1>..<h6> 标签
------------------------
``<h1>..<h6>`` 标签用于文档识别，它创建一个区段。有时 ``<h>`` 标签会出现在文档右侧，这依靠于您的文档的组织方式。如果能按顺序使用则更好。

错误用法::

    <strong>This is my Smashing Heading</strong><p>This is my xyz description.</p>

正确用法::
	
    <h1>This is my Smashing Heading</h1><p>This is my xyz description.</p>

12. 糟糕的 <marquee> 和 <blink>
-------------------------------
.. figure:: images/Look-at-Me1.jpg

可以说， ``<marquee>`` 和 ``<blink>`` 是另外一种让 WEB 页面丑陋的方式。假如你想让一些内容引起他人的注意，您应当使用其他方式，决不要用文本闪烁和移动，这是真正让人讨厌的方式。


