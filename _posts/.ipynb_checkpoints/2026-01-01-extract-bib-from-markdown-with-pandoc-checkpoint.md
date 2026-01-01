---
title: 'Extract bibliography from markdown with Pandoc'
excerpt: 'This post demonstrates the workflow of extracting bibliography from markdown.'
date: 2026-01-01
permalink: /posts/extract-bib-from-markdown-with-pandoc/
tags:
  - markdown
  - pandoc
  - latex
  - tutorial
---

I have been using Obsidian for most of my works since few years. From simple note taking, creating presentation, and writing manuscript draft. Recently, when I was about to submitting the manuscript in a Latex format, I got several issues related to bibliography. 

I did not want to include all items in my Zotero library in the bibtex. I just wanted to use the bibliography that were cited in my manuscript. So, I looked for the solutions through internet and talking with AI copilot. Here is the workflow that works for me.

Extract bibliography
======

You are going to need the following setup:

- Pandoc version 3.5 above
- Lua filter
- Complete bibliography file extracted from Zotero.

That complete bibliography file enables my Obsidian to cite directly from my Zotero library. To generate this file, you will require to install `Better Bibtex` plugin in Zotero. It is automatically updated whenever there is an update in the library.

Create a file naming `extract-bib.lua` with the following code:

```
function Pandoc(d)
  d.meta.references = pandoc.utils.references(d)
  d.meta.bibliography = nil
  return d
end
```

Place that file in the same directory with your markdown file. Of course you can put it elsewhere and use relative path. Then run the following command in the command shell.

```
pandoc --bibliography=[complete-bibliography.yaml] --lua-filter extract-bib.lua manuscript.md --to=bibtex -o references.bib
```

You can replace `complete-bibliography.yaml` with the relative path of your bibliography file. In this case, I use `yaml` type while you may choose different type to extract your Zotero library.

Get DOIs corrected
======

After the cited bibliography extracted, I found that some of the entries were not conform the requirement of `natbib`, which is required by the journal to compile the bibtex. For instance, the bibtex contains no DOI entries.

To find DOI automatically using the bibtex, use a python code from this repository [https://github.com/ramonium/AutomaDOI](https://github.com/ramonium/AutomaDOI/tree/main).

You can verify the updated DOIs in the bibtex through this website [https://www.doi2bib.org](https://www.doi2bib.org).

Reformat bibtex
------

Sometimes you may encounters another issue related to UTF-8 encoding. This happens when your bib entries contains special characters, like å, ø, æ, inherent in authors' name. There is no work around for this issue. You need to replace those character with Bibtex-compliant format. 

Maybe you can also try to include package to solve it. See [https://overleaf.com/learn/latex/International_language_support](https://overleaf.com/learn/latex/International_language_support).

**Optional**

If you want to reformat the bibtex into biblatex with braces, you can just copy paste those bib entries to the following website:

[https://flamingtempura.github.io/bibtex-tidy](https://flamingtempura.github.io/bibtex-tidy)

Once you click the `Tidy` button, it will automatically beautify your bib entries. 