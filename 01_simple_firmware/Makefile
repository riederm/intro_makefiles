firmware: main.o uart.o led.o
	gcc build/main.o build/uart.o build/led.o -o build/firmware

main.o: main.c uart.h led.h
	gcc -c main.c -o build/main.o

uart.o: uart.c uart.h
	gcc -c uart.c -o build/uart.o

led.o: led.c led.h
	gcc -c led.c -o build/led.o

.PHONY: clean
clean:
	rm -rf build/*
