---
layout: post
title:  "css层叠样式表-box-sizing"
date:   2020-09-26 14:26:51 +0800
categories: [web]
tags: [css]	
	
---
box-sizing的属性默认值是 content-box，其设置的宽度值即为内容区宽度值，设置的边框和内边框会被增加到最后绘制出来的元素宽度中。
```

	.parents {
		width: 300px;
		height: 400px;

		border: solid rebeccapurple 10px;
	}

	.child {
		box-sizing: content-box;
		width: 100%;
		border: solid blue 10px;
		padding: 5px;
		margin-top: 20px;
	}

```

![avatar](/assets/img/sample/css_box_sizing_content-box.jpg)

border-box设置的宽度包括边框和内边距，设置的宽度=实际宽度 + border + padding。
 
```
	.parents {
		width: 300px;
		height: 400px;

		border: solid rebeccapurple 10px;
	}

	.child {
		box-sizing: border-box;
		width: 100%;
		border: solid blue 10px;
		padding: 5px;
		margin-top: 20px;
	}
	
```

