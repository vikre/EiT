build:
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

lint:
  @chktex Rapport.tex
  @node node_modules/mllc/cli.js '**/*.tex'

setup:
  npm install mllc

.PHONY: clean out lint
