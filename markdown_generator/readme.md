# BibTeX to markdown generator

The default generator files have been moved to unused directory. Current markdown generator was forked from [Dr. Michele C. Weigle](https://weiglemc.github.io/) repository.

## Python version generator
* `wanprabu.bib` contains my publications exported from Google scholar
* `bib2md.py` is a Python script to generate markdown files using bibtex input file. Edit this file to change the input file and output directory. The default output directory is set to `_publications/` 
* `bibtexref3_md.py` is a Python library used along with `bib2md.py` to perform the conversion
* To run the generator in terminal, execute `% python3 bib2md.py`

## Old Jupyter notebook generator
These .ipynb files are Jupyter notebook files that convert a TSV containing structured data about talks (`talks.tsv`) or presentations (`presentations.tsv`) into individual markdown files that will be properly formatted for the academicpages template. The notebooks contain a lot of documentation about the process. The .py files are pure python that do the same things if they are executed in a terminal, they just don't have pretty documentation.




