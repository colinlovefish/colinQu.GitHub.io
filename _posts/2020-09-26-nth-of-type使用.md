---
layout: post
title:  "nth-of-type使用"
date:   2020-09-26 14:26:51 +0800
categories: [web]
tags: [css]	
---

   <strong> nth-of-type(): </strong>   这个CSS伪类，针对具有一组兄弟节点的标签，用n来筛选一组兄弟节点的位置。在多个css同节点中，区分不同兄弟节点，用于做节点特殊处理。
   
```

     &:nth-of-type(3){
	    a{
		    .downloadButton{
			    :global(.icon){
				    font-size: 14px;
				}
			}
		}
	}

```

<strong> :nth-last-of-type(an+b) </strong> 基本上和 <strong> :nth-of-type </strong>  但是是从结尾处反序计数。

