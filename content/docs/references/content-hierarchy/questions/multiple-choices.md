---
title: "多选"
date: 2021-11-14T15:47:14+08:00
weight: 2
---

# ☑️ 多选

## 数据结构

```yaml
kind: MULTIPLE_CHOICES
config:
	stems:
		- text: 通常下列哪些选项会形成人脑中的长期记忆？
	choices:
		A:
			text: 使用九键键盘打字
		B:
			text: 一则大快人心的新闻
		C:
			text: 坐地铁先下后上
	answers:
		- A
		- C
	explains:
		- text: 通常对我们的生活长期有意义的感知信号会在人脑中形成长期表达，一些即时有效，用后即废的信号会形成短期表达
```

字段说明：

| 字段名     | 类型                                                         | 说明                                                         |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `choices`* | Map<string, [Content](/nerds-docs/docs/content-hierarchy/questions/#内容单元)> | 键为选项标识，一般依次使用大写字母 A-Z；值为选项内容，可以使用任意支持的内容单元 |
| `answers`* | List<string>                                                 | 由 `choices` 中出现过的任意一个或多个键组成                  |

