CC     = gcc
CFLAGS = -Wall -O2

SRCS = main.c uart.c led.c
OBJS = $(SRCS:%.c=build/%.o)

build/firmware: $(OBJS)
	$(CC) $^ -o $@

build/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

.PHONY: clean
clean:
	rm -rf build/*
