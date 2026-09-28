# Makefile for C projects

# Compilation flags
CC = gcc
CFLAGS = -Wall -Wextra

# Executable file
TARGET = a.out
ifeq ($(TARGET),a.out)
$(warning << Makefile >> Please set the TARGET variable to the desired executable name!)
endif

# Source files and object files
SRCS = $(wildcard *.c)
OBJS := $(SRCS:.c=.o)

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)
