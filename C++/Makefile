# Makefile for projects

# Compliation flags (Using C++20)
CXX = g++
CXXFLAGS = -Wall -Wextra -std=c++20

# Executable file
TARGET = a.out
ifeq ($(TARGET),a.out)
$(warning << Makefile >> Please set the TARGET variable to the desired executable name!)
endif

# Source files and object files
SRCS = $(wildcard *.cpp)
OBJS = $(SRCS:.cpp=.o)

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CXX) $(CXXFLAGS) $^ -o $@

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)
