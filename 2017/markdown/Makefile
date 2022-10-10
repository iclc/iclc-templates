all: iclc2017.pdf iclc2017.html

iclc2017.html: iclc2017.txt references.bib
	pandoc --template=pandoc/iclc.html --filter pandoc-citeproc --number-sections iclc2017.txt -o iclc2017.html

iclc2017.pdf: iclc2017.txt references.bib pandoc/iclc.latex pandoc/iclc.sty
	pandoc --template=pandoc/iclc.latex --filter pandoc-citeproc --number-sections iclc2017.txt -o iclc2017.pdf

iclc2017.docx: iclc2017.txt references.bib
	pandoc --filter pandoc-citeproc --number-sections iclc2017.txt -o iclc2017.docx

iclc2017x.pdf: iclc2017.txt references.bib pandoc/iclc.latex pandoc/iclc.sty
	pandoc --template=pandoc/iclc.latex --filter pandoc-citeproc --number-sections iclc2017.txt --latex-engine=xelatex -o iclc2017x.pdf
