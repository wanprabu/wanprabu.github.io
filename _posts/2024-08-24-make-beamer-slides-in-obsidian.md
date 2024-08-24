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
The following is a sample of markdown file I used. The first part contains YAML metadata, put within `---` marker.

```markdown
---
category: slide
title: Course Code - Longer course name here
subtitle: "Build your first beamer slides using markdown and Pandoc"
date: 2024-08-23	
aspectratio: "169"
author: Put your name here
institute: "Department of Industrial Engineering\r \\newline Faculty of Engineering Science and Technology"
theme: CambridgeUS
colortheme: dolphin
toc: "true"
toc-title: Outlines
numbersections: "false"	
titlegraphic: UiT-logo.png
titlegraphicoptions: height=1cm
---

# Introduction
This presentation contains some guidelines for creating beamer slides

## Background
* Important point
* Point 2

1. Order with number
2. Other points

## Objective

#### Main objective
The primary purpose of this guideline is to provide a brief tutorial for creating beamer slides

# Methods
![Flow chart of methods. You may replace with image from your local machine](https://assets-global.website-files.com/6184b461a39ff13bfb8c0556/618b7df8770a665e3c5cd9d2_sample-flowchart.jpeg){height=70%}


## Algorithm
```jsx
Bot.send("Are you going out to play?")
async function respond(inputText){
    if (inputText == "yes"){
        Bot.send("Wear a hat");
    }
    else {
        Bot.send("ok");
    }
}

# Results
::: columns

:::: column
Left column content
1. Item A
2. Item B
3. Item C
::::

:::: column
\small
This column displays smaller content

\footnotesize
This text is even much smaller
::::

:::

# Conclusion
- End of slides
- No more content

\centering
\Huge
\textcolor{Red}{Thank You}

```

I enclosed a preamble containing TeX file to setting some formatting elements.

How to build
------

`pandoc -t beamer presentation.md --slide-level 3 -H preamble.tex -o presentation.pdf`
