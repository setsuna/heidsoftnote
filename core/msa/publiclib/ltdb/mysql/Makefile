SHELL=/bin/sh
DBDIR = /usr/local/mysql
DBINCLUDE = -I$(DBDIR)/include/mysql
DBLIB = $(DBDIR)/lib/mysql/libmysqlclient.a

all: ltdb.o
	ar rv ltmysql.a ltdb.o
	cp ltdb.o 					../../lib/
	cp ../ltdb.h 				../../include/
	cp ../dbmysql.h 		../../include/


ltdb.o: ltdb.c
	gcc -c ltdb.c -I../ -I../../include  $(DBINCLUDE)
	
install:
	cp ltdb.o 					../../lib/
	cp ../ltdb.h 				../../include/
	cp ../dbmysql.h 		../../include/


