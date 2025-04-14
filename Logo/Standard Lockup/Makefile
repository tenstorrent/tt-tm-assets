SVGs=$(wildcard svg/*.svg)
PNGs=$(SVGs:svg/%.svg=png/%.png)

all: $(PNGs) 
	
png/%.png: svg/%.svg
	inkscape \
		-h 256 \
		$^ \
		-o $@
clean:
	rm -rf *.ico
