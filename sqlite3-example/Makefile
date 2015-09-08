
CC=g++
CFLAGES= -I./3rd/SQLiteCpp/
LFLAGES= -L. 3rd/SQLiteCpp/libsqlite3.a -lsqlite3


example:main.o libsqlite3.a
	$(CC) $< $(LFLAGES) -o $@

libsqlite3.a:
	$(MAKE) -C ./3rd/SQLiteCpp/

%.o:%.cpp
	$(CC) -c $(CFLAGES) $< -o $@


clean:
	rm *.o example 
	$(MAKE) clean -C ./3rd/SQLiteCpp/

