# @file Makefile
# @author Cameron Tucker
# @date 2024-09-17
# @brief Builds employee program with warnings, flags, and manages all
# object files. 



CC = g++ 								#C++ compiler
TARGET = employee 							#final executable
CFLAGS = -c -Wall -Wextra						#shows all errors and warnings

all: $(TARGET)


$(TARGET): main.o Employee.o Officer.o Supervisor.o			#links all object files to single executable 
	$(CC) main.o Employee.o Officer.o Supervisor.o -o $(TARGET)

main.o: main.cpp							#compiles into object files 
	$(CC) $(CFLAGS) main.cpp

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) Supervisor.cpp

clean:									#cleans up object and backup files 
	rm -f *.o *~ $(TARGET)
