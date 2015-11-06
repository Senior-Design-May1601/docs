TEX=$(wildcard *.tex)
PDF=Presentation-11-10
BUILD=pdflatex
SRC=Presentation-11-10

all: ${PDF}

${PDF}: ${TEX}
	${BUILD} ${SRC}
	${BUILD} ${SRC}

clean:
	rm -rf *.pdf *.aux *.log *.out *.glg *.glo *.gls *.ist *.log *.lot *.toc *.xdy *.glsdefs *.vrb *.nav *.snm

.PHONY: clean
