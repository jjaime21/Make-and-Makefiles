/**
 * @file Makefile
 * @author Jose Jaime
 * @date 2025-02-14
 * @brief Practice writing Makefiles for a given project
 * 
 * Makefile for a small inheritance project
 */

CC = g++
CFLAGS = -g -Wall -Wextra

default: Main

Main: main.o
	$(CC) $(CFLAGS) -o Main main.o

main.o: main.cpp
	$(CC) $(CFLAGS) -c main.cpp

clean:
	$(RM) Main *.o *~
