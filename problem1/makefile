

CPP = g++
CFLAGS = -Wall --pedantic-errors

program: main.o TrianglePrinter.o funcs.o
	${CPP} main.o TrianglePrinter.o funcs.o -o program

%.o: %.cpp
	${CPP} ${CFLAGS} -c $<

.PHONY: debug clean

debug: CFLAGS = -g -Wall --pedantic-errors
debug: program

main.o: main.cpp funcs.h
	${CPP} ${CFLAGS} -c main.cpp

TrianglePrinter.o: TrianglePrinter.cpp TrianglePrinter.h
	${CPP} ${CFLAGS} -c TrianglePrinter.cpp

funcs.o: funcs.cpp funcs.h
	${CPP} ${CFLAGS} -c funcs.cpp

clean:
	-@rm -f program
	-@rm -f *.o



