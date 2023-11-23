all: iclc2024x.pdf iclc2024.html

clean:
	rm iclc2024.pdf iclc2024.html

iclc2024.html: iclc2024.md references.bib
	pandoc --template=pandoc/iclc.html --citeproc --number-sections iclc2024.md -o iclc2024.html

iclc2024.pdf: iclc2024.md references.bib pandoc/iclc.latex pandoc/iclc.sty
	pandoc --template=pandoc/iclc.latex --citeproc --number-sections iclc2024.md -o iclc2024.pdf

iclc2024.docx: iclc2024.md references.bib
	pandoc --citeproc --number-sections iclc2024.md -o iclc2024.docx

iclc2024x.pdf: iclc2024.md references.bib pandoc/iclc.latex pandoc/iclc.sty
	pandoc --template=pandoc/iclc.latex --citeproc --number-sections iclc2024.md --pdf-engine=xelatex -o iclc2024x.pdf
