---
title: "题目类型"
date: 2021-11-14T15:35:04+08:00
# bookComments: false
# bookSearchExclude: false
---

> TL;DR 👉🏻 笨学指南目前支持的题型包括：单选、多选、填空、自答。

## 标准字段

每个题目都至少包含两个字段：题目类型 `kind` 和题目配置 `config`。其中题目配置中至少包含题干 `stems` 和解答 `explains`。

```yaml
kind: QUESTION_KIND
config:
	stems:
	explains:
```

## 单选题

```yaml
kind: SINGLE_CHOICE
config:
	stems:
		- kind: MARKDOWN
		  text: |
		  	38 位外科住院医师作为被试者参加了一项实验：学习四节显微外科课程，讲授如何重连微小血管。其中 19 位
		  	医师在一天内听完所有课程，剩下的医师在一周内逐步学完所有课程。一个月后，他们被要求参加一次测验：为
		  	小白鼠重连血管。

		  	你觉得哪组医师的表现更好？
	choices:
		A:
			kind: TEXT
			text: 一天内听完所有课程的医师
		B:
			kind: TEXT
			text: 一周内听完所有课程的医师
	answer: B
	explains:
		- kind: TEXT
		  text: >
		  	测验结果标明，一周内听完所有课程的医师在所有评价指标上的表现都优于一天内完成所有课程的医师。人脑
		  	神经通路的建立过程需要不断强化，有间隔、有遗忘、再回忆的过程可以帮助人脑建立更强健的网络。
```

单选题特有的两个字段是 `choices` 和 `answer`。

## 多选题

```yaml
kind: MULTIPLE_CHOICES
config:
	stems:
		- kind: TEXT
		  text: >
		  	通常下列哪些选项会形成人脑中的长期记忆？
	choices:
		A:
			kind: TEXT
			text: 使用九键键盘打字
		B:
			kind: TEXT
			text: 一则大快人心的新闻
		C:
			kind: TEXT
			text: 坐地铁先下后上
	answers:
		- A
		- C
	explains:
		- kind: TEXT
		  text: 通常对我们的生活长期有意义的感知信号会在人脑中形成长期表达，一些即时有效，用后即废的信号会形成短期表达
```

多选题特有的两个字段是 `choices` 和 `answers`。

## 填空题

```yaml
kind: FILL_IN_THE_BLANKS
config:
  stems:
	target: |
		So no one ${verb} you life was gonna be this way
	fillers:
		verb: told
	explains:
		- kind: TEXT
		  text: >
				"没有人曾告诉过你，生活就是这样的"
```

填空题特有的两个字段是 `target` 和 `fillers`。其中 `target` 使用的是 Javascript 的[字符串模板](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)。

### 自答题

```yaml
kind: YOU_TELL
config:
	stems:
		- kind: TEXT
		  text: >
		    我们称一些能瞬间理解、记忆的内容为瞬间可检索，人脑瞬间可检索的容量十分有限。那么如果你想让你脑中可
		    检索的信息容量变大，可以怎么做？
	explains:
		- kind: TEXT
		  text: >
		  	尽管脑中瞬间可检索的容量有限，但我们可以以这些瞬间可检索的内容为线索，建立它们与其它信息的联系，
		  	利用间接检索的方式扩大脑中的可检索信息容量。
```

自答题除了题干和解答外，没有其它字段。

## 参考文献

* [MDN: Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
