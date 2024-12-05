SVGs=$(wildcard *.svg)
ICOs=$(SVGs:%.svg=%.ico)

all: $(ICOs) favicon.ico
	
%.ico: %.svg
	magick \
		-density 300 \
		-define icon:auto-resize=256,128,96,64,48,32,16 \
		-background none \
		$^ \
		$@
favicon.ico: favicon-purple.ico
	cp favicon-purple.ico favicon.ico

clean:
	rm -rf *.ico
