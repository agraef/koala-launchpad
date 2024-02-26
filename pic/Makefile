
# This needs pikchr (https://pikchr.org) and (optionally) ImageMagick (convert).

all: conn.svg

%.svg: %.pikchr
	pikchr --svg-only $< > $@

%.png: %.svg
	convert -density 1200 $< $@

# crop screenshots
crop:
	for x in patchbay*.png; do cp $$x $$x~; magick $$x -crop +50+80 -crop -100-0 $$x; done

clean:
	rm -f *.svg
