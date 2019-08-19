notebookentries := $(shell grep '\\input{.*entries' notebook.tex | sed 's/^.*\\input{\(.*\.tex\).*/\1/')

all: notebook.pdf

notebook.pdf: notebook.tex $(notebookentries)
	pdflatex -draftmode notebook.tex
	pdflatex notebook.tex
	rm notebook.log notebook.out notebook.toc notebook.aux
