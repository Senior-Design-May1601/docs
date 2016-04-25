TEX=$(wildcard *.tex)
PDF=May1601-Final-Report
BUILD=pdflatex
SRC=May1601-Final-Report

all: ${PDF}

${PDF}: ${TEX}
	${BUILD} ${SRC}
	${BUILD} ${SRC}
	${BUILD} ${SRC}

clean:
	rm -rf *.pdf *.aux *.log *.out *.glg *.glo *.gls *.ist *.lof *.lot *.toc *.xdy *.glsdefs

.PHONY: clean
