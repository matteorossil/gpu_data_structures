# Variables
EXECUTABLE = driver
SOURCE = driver.cu hashmap_gpu.cu kernels.cu utils.cu 
FLAGS = -I. -O1
NVCC = nvcc

# Default target
all: $(EXECUTABLE)

# Build the driver executable
$(EXECUTABLE): $(SOURCE)
	$(NVCC) --std=c++14 $(FLAGS) -o $(EXECUTABLE) $(SOURCE)

# Clean up the build
clean:
	rm -f $(EXECUTABLE)

# Run the executable
run: $(EXECUTABLE)
	./$(EXECUTABLE)

# PHONY targets
.PHONY: all clean run
