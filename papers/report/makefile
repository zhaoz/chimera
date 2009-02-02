# $Id: makefile,v 1.2 2006/05/02 21:30:41 krishnap Exp $
# Matthew Allen

all: report.pdf

FILES = api.tex conclusion.tex design.tex introduction.tex report.tex results.tex design.eps

clean:
	rm -f *.dvi *.ps *.aux *.log *.pdf

.SUFFIXES: .dvi .ps
.dvi.ps:
	dvips -o $*.ps $*.dvi

.SUFFIXES: .tex .dvi
.tex.dvi:
	latex $*.tex
	bibtex $*
	latex $*.tex
	latex $*.tex

.SUFFIXES: .ps .pdf
.ps.pdf:
	ps2pdf $*.ps $*.pdf

report.pdf: report.ps

report.dvi: $(FILES)
