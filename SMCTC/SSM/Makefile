CC = g++
C = ssmEx.cpp pffuncs.cpp 
O = ssmEx.o pffuncs.o
H = pffuncs.h

CPPFLAGS = -I~/src/smctc/include -L~/src/smctc/lib 
LFLAGS =  -I~/src/smctc/include -L~/src/smctc/lib  $(shell gsl-config --libs)

all: ssmEx

ssmEx: $(C) $(H)
	$(CC) $(CCFLAGS) -c $(C)
	$(CC) $(O) -lsmctc $(LFLAGS) -o ssmEx

ssmExx: $(C) $(H)
	$(CC) $(C) -o ssmExx -lsmctc -lgsl -lgslcblas 

clean:
	-rm *.o
	-rm *~
	-rm ssmEx
