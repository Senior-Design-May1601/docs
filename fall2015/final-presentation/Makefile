TEX=$(wildcard *.tex)
PDF=May1601-Final-Presentation
BUILD=pdflatex
SRC=May1601-Final-Presentation

all: ${PDF}

${PDF}: ${TEX}
	${BUILD} ${SRC}
	${BUILD} ${SRC}

clean:
	rm -rf *.pdf *.aux *.log *.out *.glg *.glo *.gls *.ist *.log *.lot *.toc *.xdy *.glsdefs *.vrb *.nav *.snm

.PHONY: clean
