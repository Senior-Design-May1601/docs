all: report.pdf

report.pdf: report.tex introduction.tex project-requirements.tex interface-and-system-description.tex work-breakdown.tex conclusion.tex ref.tex title.tex
	pdflatex report.tex
	pdflatex report.tex

clean:
	rm -rf *.pdf *.aux *.log *.out

.PHONY: clean
