# Compiler and flags
CXX = g++
CXXFLAGS = -std=c++23 -Wall -Wextra -pedantic

# Project name
TARGET = hello-world

# Source files (automatically find all .cpp files in current directory)
SRCS = $(wildcard *.cpp)
OBJS = $(SRCS:.cpp=.o)

# Main target
$(TARGET): $(OBJS)
	$(CXX) $(OBJS) -o $(TARGET)

# Generate object files
%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

# Clean up
clean:
	rm -f $(OBJS) $(TARGET)

# Clean and rebuild
rebuild: clean $(TARGET)