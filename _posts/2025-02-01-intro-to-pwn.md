---
title: "intro-to-pwn — week 1: your first overflow"
categories: [teaching, pwn]
tags: [course, pwn]
description: "From a vulnerable C program to controlling the instruction pointer."
---

Welcome to week 1. By the end you'll overwrite a return address and redirect
execution.

## Setup

```bash
sudo apt install gdb gcc
```

## The vulnerable program

```c
#include <string.h>
void win() { /* ... */ }
int main(int argc, char **argv) {
    char buf[64];
    strcpy(buf, argv[1]);   // no bounds check
    return 0;
}
```

## Exercise

Find the offset to the saved return address. Hint: use a cyclic pattern.
