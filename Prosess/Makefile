build: out lint
	pdflatex --output-directory out/ Rapport.tex
	bibtex out/Rapport.aux
	pdflatex --output-directory out/ Rapport.tex
	pdflatex --output-directory out/ Rapport.tex
out:
	@mkdir -p out

clean:
	@rm -fR out

open: build
	@open out/Rapport.pdf

setup:
	npm install mllc

.PHONY: clean out lint
