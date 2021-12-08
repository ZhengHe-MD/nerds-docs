---
title: "简答"
date: 2021-11-14T15:47:14+08:00
weight: 4
---

# ✍🏻 简答

## 数据结构

```yaml
kind: SHORT_ANSWER
config:
	stems:
		- text: |
				怎么理解 Paul Graham 说的 "Keep Your Identity Small"？
  bullets:
  	- 你给自己加上越多的身份标签，你就是一个越愚蠢的人
  	- 带着身份标签的讨论通常没有收获
  	- 让你的身份标签尽量少是最优策略
```

字段说明：

| 字段名     | 类型         | 说明                                 |
| ---------- | ------------ | ------------------------------------ |
| `bullets`* | List<string> | 要点列表，系统会根据要点自动判定正误 |
