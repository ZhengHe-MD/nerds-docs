---
title: "填空"
date: 2021-11-14T15:47:14+08:00
weight: 1
---

# 🪣 填空

## 数据结构

```yaml
kind: FILL_IN_THE_BLANKS
config:
  stems:
  	- text: So no one ${verb} you life was gonna be this ${noun}
	fillers:
		verb: told
		noun: way
	random: true
	explains:
		- kind: TEXT
		  text: >
		  	歌词原文翻译是: 没有人曾告诉过你，生活就是这样的
```

字段说明：

| 字段名     | 类型                | 说明                                                         |
| ---------- | ------------------- | ------------------------------------------------------------ |
| `fillers`* | Map<string, string> | 键为 `target` 中的变量；值为对应的答案文本                   |
| `random`   | bool                | false 表示需要完成所有填空 (默认)；true 表示只需完成随机指定的一个填空 |

题干中待填空的文本格式使用 JavaScript 的[字符串模板](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)。

## 参考资料

* [MDN: Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)