CFLAGS = -Wall -Werror
CFLAGS += -O3
.PHONY: all format clean

all: reverse_test

format:
	clang-format -style=Google -i reverse.c

clean:
	rm -f reverse_test

reverse_test: test_reverse.c reverse.c reverse.h
	gcc $(CFLAGS) $^ -o $@