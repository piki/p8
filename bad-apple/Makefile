FRAMESKIP=1
WIDTH=16
ENCODING=age

# or:
# FRAMESKIP=8
# WIDTH=32
# ENCODING=plain

bad_apple.p8: img/output000040.png p8-encode
	bundle install
	(./p8-encode $(FRAMESKIP) $(WIDTH) $(ENCODING) img/output*.png; cat ba-sections) > $@

img/output000040.png:
	mkdir -p img
	ffmpeg -i "bad apple.m4v" -vf fps=30 "img/output%06d.png"
