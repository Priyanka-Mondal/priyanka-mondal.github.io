#Simple Makefile for DecentBDF

MAIN = priyanka
MAIN_TEX = $(MAIN).tex
MAIN_AUX = $(MAIN).aux 

all: cv

cv:
	pdflatex $(MAIN_TEX)
	#bibtex $(MAIN_AUX)
	#pdflatex $(MAIN_TEX)
	#pdflatex $(MAIN_TEX)
	#mv $(MAIN).pdf cv.pdf

clean:
	-rm -f *.aux
	-rm -f *.log
	-rm -f *.bbl
	-rm -f *.blg
	-rm -f *.out




