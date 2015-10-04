TEX=$(wildcard *.tex)
PDF=report.pdf
BUILD=pdflatex
SRC=report.tex

all: ${PDF}

${PDF}: ${TEX}
	${BUILD} ${SRC}
	${BUILD} ${SRC}

clean:
	rm -rf *.pdf *.aux *.log *.out

.PHONY: clean
