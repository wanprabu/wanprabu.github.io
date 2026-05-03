---
title: 'Make a clean CV with markdown and google sheet'
excerpt: 'Building a clean CV using markdown and google sheet'
date: 2026-05-03
permalink: /posts/make-cv-with-markdown
tags:
  - markdown
  - cv
  - workflow
  - tutorial
---

Recently I wanted to update my old CV. However, this time I did not want to manually update every item. Maintaining a CV is quite tedious routine. As when anytime I wanted to make any changes, I had to change the formating and even the entry orders. This usually will make the document getting messy. 

Finally, I found a handy package [datadrivencv](https://nickstrayer.me/datadrivencv/) which can automatically convert your CV details in the form of google sheet into a beautiful and clean markdown format. The markdown file can be rendered into a html file, which allows us to print or save as PDF document.

The workflow to create a CV using this package is as follows:

1. Prepare your CV entries in the google sheet format by simply copy the [sample](https://docs.google.com/spreadsheets/d/14MQICF2F8-vf8CKPF1m4lyGKO6_thG-4aSwat1e2TWc/edit#gid=917338460) data. Then, adjust the entries as your need. If you are reluctant to use google sheet, you may use a `.csv` file.
2. The package is written in R, so you gonna need to install R and R studio for the sake of simplicity.
3. To install the package, you require to install `devtools` or `remote` and `pagedown` package.
4. Follow the guideline in the package reference by running the `use_datadriven_cv` function. It will produce several files (i.e., markdown, r, css). If you work on unix based systems, you may need to rename the file extension into small caps because the function is case sensitve.
5. Run the `render` function to produce a cv in html format. To make a PDF document, you can simply print out from the html.

The final output of this workflow can be found in my [CV](/_pages/cv.html).
