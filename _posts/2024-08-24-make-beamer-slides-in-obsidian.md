---
title: 'Make beamer slides using Obsidian and Pandoc'
excerpt: 'Finally! This is my experience of building beamer slides presentation using markdown and Pandoc in Obsidian. I recently made a success when building beamer slides using Obsidian.'
date: 2024-08-24
permalink: /posts/make-beamer-slides-in-obsidian/
tags:
  - tutorial
  - obsidian
  - category2
---

I recently made a success when building beamer slides using [Obisidian](https://obsidian.md/). Though I am familiar of using pure LaTeX to make a beamer presentation, this markdown offers a better idea by using slightly less code. The conversion of markdown file was handled very well by the power of Pandoc. 

It seems ridiculous to make just make a presentation using all these methods. I could simply jump to a more convenient software like PowerPoint. But somehow this routine is painful to lay out every slide. Then you end up with inconsistent slide format. Nonetheless, I still use PowerPoint occasionally for some simple graphic editing works.

After so many trial and errors, the presentation material was finally built. Previously, I have made a beamer template in Obsidian. But for some reasons the template was not able to produce the results as I expected. So I made some improvements in the template and make a preamble file to customise the slide format.

Requirements
======
1. You need [Pandoc](https://pandoc.org/) as an engine to convert `.md` file to beamer slides in `.pdf` format
2. As a windows user, I use [MikTeX](https://miktex.org/) as a TeX package manager
3. Any markdown editors work fine. But personally I use my favourite Obsidian

Write your slides in markdown
======
The following is a sample of markdown file I used. The first part contains YAML metadata, put inside `---` marker. The metadata information will be parsed by Pandoc to produce TeX file as a basis for beamer slides conversion into `.pdf` file. For example, `titlegraphic` contains image shown at the slide title.

```markdown
---
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
```

There are tons of themes available for beamer presentation. Choose a suitable theme [here](https://hartwork.org/beamer-theme-matrix/). You may also set other variables for this metadata. Check the [documentation](https://pandoc.org/MANUAL.html#variables-for-beamer-slides) for furter information. 

The first Heading indicated by `#` marker defines a new section in the presentation. Accordingly, the second Heading will be converted as a subsection. 

To specify the slide structure, you can set `--slide-level` option. The default level is 2. But in this example I used 3 levels. Please refer to the [documentation](https://pandoc.org/MANUAL.html#structuring-the-slide-show) for more information.

```markdown
# Introduction
This presentation contains some guidelines for creating beamer slides

## Background
* Important point
* Point 2

1. Order with number
2. Other points
```

Since I used 3 slide-levels, Heading 4 in this below example will turn into a block. 
```markdown
## Objective

#### Main objective
The primary purpose of this guideline is to provide a brief tutorial for creating beamer slides
```

Inserting an image simply uses `![Figure Caption](path-to-image/figure.png)` syntax. If you need to specify the image size, adjusting the `height` or `width` is possible at the end of syntax.
```markdown
# Methods
![Flow chart of methods. You may replace with image from your local machine](https://assets-global.website-files.com/6184b461a39ff13bfb8c0556/618b7df8770a665e3c5cd9d2_sample-flowchart.jpeg){height=70%}

## Some theorem
The well known Pythagorean theorem $x^2 + y^2 = z^2$ was  proved to be invalid for other exponents. 

**Geometric distribution**

$P[X=k] = (1-p)^{k-1}p, \quad k=1,2,\dots$

$E[X]=\dfrac{1}{p}, \quad V[X]=\dfrac{1-p}{p^2}$

```

This slide shows an example code highlighting. List of languages supported by Pandoc can be checked by typing this command in the terminal `pandoc --list-highlight-languages`
```markdown
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
```

Beamer allows for dividing the slide content into columns. To do so, follow the below sample for producing two equal width columns. First, you need to specify the columns using `::: columns` and close with `:::`. Then, within the block, specify the column block with `::::` *put whatever content in this column blok* `::::`. 

It is also possible to specify the column wdith. Using this sytaxy `:::: {.column width=40%}`, you will get a column with 40% of width.
```markdown
# Results
## Column equal width
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
```

You are allowed to use some LaTeX syntax inside a markdown file. 
- `\centering` will make a center aligned content
- `\Huge` will make your text a lot bigger
- `\textcolor{}{}` to produce coloured text

```markdown
# Conclusion
- End of slides
- No more content

\centering
\Huge
\textcolor{Red}{Thank You}

```

Preamble file
------
I enclosed a [preamble](/files/beamer-preamble.tex) containing TeX file to customise some formatting elements. This file is separated from the markdown and used during the compile process.

How to build
======
Run the following command in the terminal to build the `.pdf` slides

`pandoc -t beamer presentation.md --slide-level 3 -H preamble.tex -o presentation.pdf`

The sample output of above code is available [here](/files/slides-with-obsidian.pdf)

Summary
======
Well, it is tiresome to make a clean and well built this markdown beamer slide template at the begining. Moreover, it is more difficult to debug compared to pure LaTeX. But once everthing are prepared well on the table, the next workflow will much easier.

In summary, I use the following workflow to produce beamer slides:
1. Make a template in Obsidian to easily automate the creation of markdown metadata and some default sections
2. Edit the preable file to customise the slide formats
3. Generate `pdf` slides using Pandoc
4. See the result and make adjustment if necessary

References: 
1. [https://lothode.pages.math.cnrs.fr/pageperso/blog/beamer-with-pandoc/](https://lothode.pages.math.cnrs.fr/pageperso/blog/beamer-with-pandoc/)
2. [https://github.com/alexeygumirov/pandoc-beamer-how-to](https://github.com/alexeygumirov/pandoc-beamer-how-to)
