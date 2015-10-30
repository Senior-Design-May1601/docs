TEX=$(wildcard *.tex)
PDF=May1601-Project-Plan.pdf
BUILD=pdflatex
SRC=May1601-Project-Plan.tex

all: ${PDF}

${PDF}: ${TEX}
	${BUILD} ${SRC}
	${BUILD} ${SRC}

clean:
	rm -rf *.pdf *.aux *.log *.out *.lof *.lot *.toc

.PHONY: clean
