---
toc: true
layout: post
Badges: true
comments: true
author: Mati Danish
categories: [hacks, markdown]
title: parallel computing hacks
---


# Hacks
> AP Classroom. Provide answers and thoughts on theoritical question form college board Video in section 4.3.  They start at about the 9 minute mark.
- Example 1

![image](https://media.discordapp.net/attachments/914072417310232616/1092179386914054195/CB_EX_1.png?width=2000&height=920)




- Example 2

![image](https://media.discordapp.net/attachments/914072417310232616/1092179387207663627/CB_EX_2.png?width=2000&height=862)

running both process one after another will take 70 seconds
but running them in parallel computing, it could take less than 25 seconds

> Data Structures.  Build a List Comprehension example
- list = [calc(item) for item in items]


``` python
strings = ["apple", "samsung", "google", "pineapple"]
string_lengths = [len(string) for string in strings]
print(string_lengths)

```

output:

``` python
[5, 7, 6, 9]
```