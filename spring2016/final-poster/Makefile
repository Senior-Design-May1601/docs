TEX=$(wildcard *.tex)
PDF=May1601-Final-Poster
BUILD=pdflatex
SRC=May1601-Final-Poster

all: ${PDF}

${PDF}: ${TEX}
	${BUILD} ${SRC}
	#bibtex ${SRC}.aux
	#${BUILD} ${SRC}
	#bibtex ${SRC}.aux
	#bibtex ${SRC}.aux
	#${BUILD} ${SRC}
	${BUILD} ${SRC}

clean:
	rm -rf *.pdf *.aux *.log *.out *.glg *.glo *.gls *.ist *.log *.lot *.toc *.xdy *.glsdefs *.vrb *.nav *.snm

.PHONY: clean
