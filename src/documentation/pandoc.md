<!-- toc -->
# Pandoc

[How to use Pandoc to produce a research paper](https://opensource.com/article/18/9/pandoc-research-paper)

create `paper.pdf` from `paper.md` and `paper.bib`

```shell
pandoc --pdf-engine latexmk -C --bibliography=paper.bib \
-V classoption=twocolumn -V papersize=a4paper -V fontsize=12pt \
-V geometry:margin=0.1in -V mainfont=Times \
-s paper.md -o paper.pdf
```

using HTML as intermedia and `wkhtmltopdf` to create PDF

```shell
pandoc -s paper.md -o paper.pdf -t html5 \
-V margin-top=0 -V margin-bottom=0 -V margin-left=0 -V margin-right=0
```
