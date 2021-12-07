---
title: "配对"
date: 2021-11-14T15:47:14+08:00
weight: 6
---

# 🧬 配对

## 数据结构

```yaml
kind: MATCHING
config:
	stems:
		- text: 连接水果及其对应的颜色
  pairs:
  	Banana: Yellow
  	Carrot: Orange
  	Blueberries: Purple
  lhs:
  	Banana:
  		text: Banana
    Carrot:
      text: Carot
    Blueberries:
    	text: Blueberries
  rhs:
  	Yellow:
  		text: Yellow
    Orange:
    	text: Orange
    Purple:
    	text: Purple
  explains:
  	- text: |
  		以下是各个水果的图片：
  		
  		![Banana](https://path/to/banana.png)
  		...
    
```

字段说明：

| 字段名   | 类型                                                         | 说明                                                         |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `pairs`* | Map<string, string>                                          | 按正确答案配对的结果，每次生成题目时会随机打乱键值           |
| `lhs`    | Map<string, [Content](/nerds-docs/docs/quiz/question_types/#内容单元)> | pairs 中的键对应的内容单元，如果不给，默认使用键对应的字符串 |
| `rhs`    | Map<string, [Content](/nerds-docs/docs/quiz/question_types/#内容单元)> | Pairs 中的值对应的内容单元，如果不给，默认使用值对应的字符串 |

