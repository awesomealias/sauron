all: images

dots = $(wildcard *.dot)
dot_pngs = $(dots:.dot=.png)

%.png: %.dot
	dot -Tpng -Gdpi=300 $< -o $@

images: $(dot_pngs)

.PHONY: clean
clean:
	rm -f $(dot_pngs)