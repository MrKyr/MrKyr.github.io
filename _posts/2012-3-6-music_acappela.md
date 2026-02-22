---
layout: post
author: kyr
date: 2012-3-6 11:12:04 +0200
title: Acappelas
description: 
category: [Coding]
tags: [linux, mac, music]
comments_id: 4
---

Here is how i've been creating acappellas on linux with [SoX](http://sox.sourceforge.net "SoX - Sound eXchange") a cross-platform command line audio utility tool that works on Linux, Windows and MacOS.

### Code:

```sh
$ soxmix -v .5 a.wav -v -.5 b.wav acapella.wav
```

That's it. `a.wav` is the main, `b.wav` is the instrumental and `acapella.wav` is the output file.  
`-v .5` means half volume. `-v -.5` means half volume inverted.  
No gui, no muss, no fuss and can easily be batched or scripted.  
Only caveat, your instrumental and main must be lined up already.  
If it's not, the resulting file will be a MESS.

***\* Use This Code at Your Own Risk!***
