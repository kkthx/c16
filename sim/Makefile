
all:	test

simulate.exe:	simulate.cc
	gcc -o $@ simulate.cc

%.o:	%.cc $(HDR)
	gcc -c -o $@ $<

.PHONY:	sim asm bin clean

test:	simulate.exe ../test.bin
	simulate ../test.bin ../test.sym

polled:	simulate.exe ../polled.bin
	simulate ../polled.bin ../polled.sym

loader:	simulate.exe ../loader.bin
	simulate ../loader.bin ../loader.sym

