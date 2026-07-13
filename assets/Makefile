TARGETS = cv.pdf
LATEXMK = latexmk
LATEXMK_FLAGS = -pdf -interaction=nonstopmode

.PHONY: all clean distclean watch

all: $(TARGETS)

%.pdf: %.tex preamble.tex
	$(LATEXMK) $(LATEXMK_FLAGS) $<

watch:
	$(LATEXMK) $(LATEXMK_FLAGS) -pvc cv.tex

clean:
	$(LATEXMK) -c $(TARGETS:.pdf=.tex)

distclean:
	$(LATEXMK) -C $(TARGETS:.pdf=.tex)
