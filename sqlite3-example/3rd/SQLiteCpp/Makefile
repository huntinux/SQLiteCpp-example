VPATH = .
SRCS = $(wildcard *.cpp ./*.cpp) 
OBJS = $(patsubst %.cpp, %.o, $(SRCS))

CFLAGES = -Wall -O3 -std=c++11 -Wno-deprecated -I. 

%.o:%.cpp
	g++ $(CFLAGES) -c  $< -o $@

libsqlite3: $(OBJS)
	ar -crv libsqlite3.a $(OBJS)
	@echo "."
	@echo "libsqlite3 make succeed."
clean:
	rm -rf *.o libsqlite3.a 
