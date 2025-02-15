# @file Makefile
# @author Jose Jaime
# @date 2025-02-14
# @brief Practice writing Makefiles for a given project 
# Makefile for compiling a small inheritance project for employees

# Compiler
CC = g++

# Target Executable Name
TARGET = employee

# Compile with all errors and warnings
CFLAGS = -c -Wall -Wextra

# Default Target
all: $(TARGET)

# Link all object files into the final executable
$(TARGET): main.o Employee.o Officer.o Supervisor.o
	$(CC) -o $(TARGET) main.o Employee.o Officer.o Supervisor.o

# Compile main.cpp into main.o
main.o: main.cpp Employee.h Officer.h Supervisor.h
	$(CC) $(CFLAGS) main.cpp

# Compile Employee.cpp into Employee.o
Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp

# Compile Officer.cpp into Officer.o
Officer.o: Officer.cpp Officer.h Employee.h
	$(CC) $(CFLAGS) Officer.cpp

# Compile Supervisor.cpp into Supervisor.o
Supervisor.o: Supervisor.cpp Supervisor.h Employee.h
	$(CC) $(CFLAGS) Supervisor.cpp

# Clean up compiled files
clean:
	$(RM) $(TARGET) *.o *~
