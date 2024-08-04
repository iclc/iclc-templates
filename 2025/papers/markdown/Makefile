all: iclc2025x.pdf iclc2025.html

clean:
	rm iclc2025x.pdf iclc2025.html iclc2025.pdf iclc2025.docx

iclc2025.html: iclc2025.md references.bib
	pandoc --template=pandoc/iclc.html --citeproc --number-sections iclc2025.md -o iclc2025.html

iclc2025.pdf: iclc2025.md references.bib pandoc/iclc.latex pandoc/iclc.sty
	pandoc --template=pandoc/iclc.latex --citeproc --number-sections iclc2025.md -o iclc2025.pdf

iclc2025.docx: iclc2025.md references.bib
	pandoc --citeproc --number-sections iclc2025.md -o iclc2025.docx

iclc2025x.pdf: iclc2025.md references.bib pandoc/iclc.latex pandoc/iclc.sty
	pandoc --template=pandoc/iclc.latex --citeproc --number-sections iclc2025.md --pdf-engine=xelatex -o iclc2025x.pdf
