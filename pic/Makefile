
# This needs pikchr (https://pikchr.org) and (optionally) ImageMagick (convert).

all: conn.svg

%.svg: %.pikchr
	pikchr --svg-only $< > $@

%.png: %.svg
	convert -density 1200 $< $@

clean:
	rm -f *.svg *.png
