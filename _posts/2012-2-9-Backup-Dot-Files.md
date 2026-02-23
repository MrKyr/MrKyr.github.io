---
layout: post
author: kyr
title: Backup Dot Files
description: Archive and compress all the hiden files from your home directory.
category: [Coding]
tags: [linux]
comments_id: 5
---

### Code:

```sh
tar --exclude={.cache,*/cache} -cpvzf dotfiles.tgz .[!.]*
```

* `tar`: The primary command for tape archive operations.
* `--exclude={.cache,*/cache}`: This option specifies patterns for files or directories to exclude from the archive.
* `.cache`: Excludes the `.cache` directory.
* `*/cache`: Excludes any directory named `cache` found at any level within the directories being archived (e.g., `dir/cache`).
* `-c`: Creates a new archive.
* `-p`: Preserves permissions (and ownership if run as root).
* `-v`: Verbosely lists the files processed.
* `-z`: Compresses the archive using gzip.
* `-f dotfiles.tgz`: Specifies the name of the archive file to create (`dotfiles2.tgz`).
* `.[!.]*`: This is a glob pattern that matches all "dotfiles" (hidden files and directories) in the current directory, except for `.` (current directory) and `..` (parent directory). It specifically looks for entries that start with a dot, followed by any character *not* a dot, and then any number of other characters.

> The order of their *arguments* is critical. Specifically, the archive filename must immediately follow `-f`, and the files/directories to be archived typically come last.


***\* Use This Code at Your Own Risk!***

