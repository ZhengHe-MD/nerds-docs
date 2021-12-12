---
title: "题目"
date: 2021-11-14T15:47:14+08:00
weight: 2
bookCollapseSection: true
---

# 题目

## 数据结构

### 内容单元

举例如下：

```yaml
# markdown
type: MARKDOWN
text: |
   如果想要掌握多种问题的内在原则，比如：
   - 计算不同形状容器的容积
   - 足球场上处理不同方向的来球
   - 识别不同的植物

   你可以怎么做？
# audio
type: AUDIO
text: https://learn-the-hard-way.cn/path/to/audio.wav
```

字段说明：

| 字段名  | 类型   | 说明                                                         |
| ------- | ------ | ------------------------------------------------------------ |
| `text`* | string | 内容文本，其含义随着 `type` 的变化而改变<br />`MARKDOWN`：符合 markdown 格式的文本<br />`AUDIO`：音频的 URL<br />`CODE_BLOCK`：代码块 |
| `type`  | string | 内容类型，目前支持 `MARKDOWN`(默认) 、`AUDIO`                |

#### 支持的 Markdown 语法

(待补充)

### 题目

举例如下：

```yaml
kind: QUESTION_KIND
config:
	stems:
		- text: |
		  	通常下列哪些选项会形成人脑中的长期记忆？
	explains:
		- text: |
				通常对我们的生活长期有意义的感知信号会在人脑中形成长期表达，一些即时有效，用后即废的信号会形成短期表达。
```

以下是所有类型题目的公共字段说明：

| 字段名     | 类型                                                         | 说明                           |
| ---------- | ------------------------------------------------------------ | ------------------------------ |
| `stems`*   | List<[Content](/nerds-docs/docs/content-hierarchy/questions/#内容单元)> | 题干，可包含任意数量的内容单元 |
| `explains` | List<[Content](/nerds-docs/docs/content-hierarchy/questions/#内容单元)> | 题解，可包含任意数量的内容单元 |

每个题型还拥有自己特殊的字段，详见各个题型的数据结构小节。

## 参考资料

* [Markdown Guide: Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
* [yaml.org](https://yaml.org/)