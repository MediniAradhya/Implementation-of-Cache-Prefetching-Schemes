CC=~/Desktop/How-to-install-SimpleScalar-on-Ubuntu/build/bin/sslittle-na-sstrix-gcc
CFLAGS=-g -O3

all: anagram Factorial Matrixmulti test-math

anagram: anagram.c
	$(CC) $(CFLAGS) -o anagram anagram.c

Factorial: Factorial.c
	$(CC) $(CFLAGS) -o Factorial Factorial.c -lm

Matrixmulti: Matrixmulti.c
	$(CC) $(CFLAGS) -o Matrixmulti Matrixmulti.c -lm

test-math: test-math.c
	$(CC) $(CFLAGS) -o test-math test-math.c -lm


test:	all
	../simplesim-0.1/sim-safe anagram words < input.txt
	../simplesim-0.1/sim-safe Factorial
	../simplesim-0.1/sim-safe Matrixmulti
	../simplesim-0.1/sim-safe test-math

distclean:
	-make clean

clean:
	rm -f anagram Factorial Matrixmulti test-math test-as *.[oia] core *~

