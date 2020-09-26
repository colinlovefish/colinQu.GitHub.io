---
layout: post
title:  "css层叠样式表iframe"
date:   2020-09-26 14:26:51 +0800
categories: [web]
tags: [css]	
---

<strong>HTML内联框架元素(<iframe>)</strong> 能够将另一个HTML页面嵌入当前页面中。

```html

<iframe id="inline"
		title="inline title"
		width="300"
		height="200"
		src="https://map.baidu.com/@12649521.59,4105848.27,12z">
	
</iframe>

<style>
	

	iframe {
		border: 1px solid black;
		width: auto;
	}

	.output {
		background: #eee;
	}


</style>

```

