################################################################################
#
#  Makefile for Tuner
#
################################################################################

GCC	= gcc
WINDRES = windres

all:	Tuner.exe

Tuner.exe:	Tuner.c Tuner.o Tuner.h

clean:
	rm *.exe

%.exe:	%.c
	$(GCC) -o $@ $(wordlist 1, 2, $^) -O2 -std=gnu99 \
		 -mwin32 -mwindows -lcomctl32 -lwinmm -lmsimg32

%.o:	%.rc
	$(WINDRES) -o $@ $<
