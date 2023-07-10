CFLAGS = -Wall -Werror
CFLAGS += -O3
.PHONY: all format clean

all: reverse_test

format:
	clang-format -style=Google -i reverse.c

clean:
	rm -f reverse_test test_reverse.o reverse.o

test_reverse.o: test_reverse.c
	$(CC) $(CFLAGS) -c $< -o $@

reverse.o: reverse.c reverse.h
	$(CC) $(CFLAGS) -c $< -o $@

reverse_test: test_reverse.o reverse.o
	gcc $(CFLAGS) $^ -o $@