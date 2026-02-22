---
layout: post
author: kyr
title: Max Cpu Load
description: Bash command line to show system's max cpu load. 
category: [Coding]
tags: [linux]
comments_id: 7
---

### Code:

```bash
$ echo -n `ps -eo pcpu,pid -o comm= \
  | sort -k1 -n -r | head -1 | awk '{ print $1 } '`"%"
```

***\* Use This Code at Your Own Risk!***
