---
layout: post
title:  "css层叠样式表span与div区别"
date:   2020-09-26 14:26:51 +0800
categories: [web]
tags: [css]	
---

   HTML <div>元素是通用流内容容器，作为一个纯粹的容器，<div>在语义上不表示任何特定内容。可以使用 class或者 id 属性自定义内容格式。<div>是一个块元素。

   HTML <span>元素是短语内容行内容器。<span>是行内元素。一般情况下，行内元素只能包含数据和其他行内元素。而块级元素可以包含行内元素和其他块级元素。这种结构上的包含继承区别可以使块级元素创建比行内元素更"大型"的结构。 <br>

   默认情况下，行内元素不会以新行开始，而块级元素会新起一行。

```scss

<body>

<div class="parents">
	<div class="child">
		<span>welcome to my blog </span>
	</div>
</div>


</body>

<style>

	.parents {
		width: 200px;
		height: 200px;
		border: solid rebeccapurple 10px;
	}

	.child {
		box-sizing: border-box;
		width: 100%;
		border: solid blue 10px;
		padding: 5px;
		margin-top: 20px;
	}


</style>

```