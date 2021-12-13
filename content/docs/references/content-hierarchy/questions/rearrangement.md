---
title: "重排"
date: 2021-11-14T15:47:14+08:00
weight: 7
---

# 📏 重排

## 数据结构

```yaml
kind: REARRANGEMENT
config:
	stems:
		- text: |
				将下面的数字从小到大重新排序
  elements:
  	A:
  		text: 1
  	B:
  		text: 3
  	C:
  		text: 2
  	D:
  		text: 4
  	E:
  		text: 5
  sorted:
  	- A
  	- C
  	- B
  	- D
  	- E
  explains:
```

字段说明：

| 字段名      | 类型                                                         | 说明                                                         |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `elements`* | Map<string, [Content](/nerds-docs/docs/content-hierarchy/questions/#内容单元)> | 键为元素唯一标识，可任意指定；值为选项内容，可以使用任意内容单元 |
| `sorted`*   | List<string>                                                 | 由 `elements` 中出现过的任意一个或多个键组成                 |

