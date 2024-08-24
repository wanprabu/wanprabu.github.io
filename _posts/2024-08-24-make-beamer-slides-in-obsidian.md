---
title: 'Make beamer slides using Obsidian and Pandoc'
date: 2024-08-24
permalink: /posts/make-beamer-slides-in-obsidian/
tags:
  - tutorial
  - obsidian
  - category2
---

I recently made a success when building beamer slides using [Obisidian](https://obsidian.md/). I am familiar of using pure LaTeX to make a 

After so many trial and errors, the presentation material was finally built. Previously, I have made a beamer template in Obsidian. But for some reasons the template was not able to produce the results as I expected. 

Requirements
======
1. You need Pandoc as an engine to convert `.md` file to `.pdf`
2. As a windows user, I use [MikTeX](https://miktex.org/) as a TeX package manager
3. 

Templates
======

How to build
------

`pandoc -t beamer presentation.md --slide-level 3 -H preamble.tex -o presentation.pdf`
