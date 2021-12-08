---
title: "跟读"
date: 2021-11-14T15:47:14+08:00
weight: 8
---

# 🗣️ 跟读

## 数据结构

```yaml
kind: LISTEN_AND_SAY
config:
	stems:
		- type: AUDIO
			text: https://path/to/the/saying/of/paulgraham.wav
  transcript: keep your identity small
```

字段说明：

| 字段名        | 类型   | 说明               |
| ------------- | ------ | ------------------ |
| `transcript`* | string | 音频对应的文本内容 |

题干 (`stems`) 中应该包含一个与 `transcript` 对应的 `AUDIO` 类型内容单元。
