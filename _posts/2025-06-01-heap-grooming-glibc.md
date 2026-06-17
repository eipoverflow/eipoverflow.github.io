---
title: "Heap grooming in glibc 2.39"
category: research
tags: [heap, glibc]
description: "Deterministic tcache layout primitives under modern allocator hardening."
---

A short intro paragraph. Everything below is just **markdown** — Jekyll
turns it into a terminal-styled page automatically. You never touch HTML.

## Background

Write your sections with normal `##` headings. Inline `code`, **bold**, and
[links](https://example.com) all get themed.

## The primitive

```c
// fenced code blocks are styled too
char *a = malloc(0x40);
free(a);
char *b = malloc(0x40);  // returns the same chunk
```

> Blockquotes render as dimmed phosphor.

## Takeaways

- bullet lists work
- so do numbered lists
- and tables, images, etc.

That's the whole workflow: write the file, commit, done.
