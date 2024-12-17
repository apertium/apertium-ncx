all:
	hfst-lexc --Werror ncx.lexc -o ncx.lexc.hfst
	hfst-twolc ncx.twol -o ncx.twol.hfst
	hfst-compose-intersect -1 ncx.lexc.hfst -2 ncx.twol.hfst -o ncx.gen.hfst
	hfst-invert ncx.gen.hfst | hfst-eliminate-flags | hfst-minimise -o ncx.mor.hfst

