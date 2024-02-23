
# This needs pikchr (https://pikchr.org) and ImageMagick (convert).

all: conn.png

%.svg: %.pikchr
	pikchr --svg-only $< > $@

%.png: %.svg
	convert -density 1200 $< $@

clean:
	rm -f *.svg *.png
