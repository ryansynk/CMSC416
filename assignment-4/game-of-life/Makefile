CXX = g++
CXXFLAGS = -std=c++11
CUDA = nvcc
CUDAFLAGS = -std=c++11 -O2 -Xcompiler "$(CXXFLAGS)"
GENCODE=--generate-code arch=compute_35,code=sm_35

TARGET = game-of-life

all: $(TARGET)

game-of-life: game-of-life.cu
	$(CUDA) $(CUDAFLAGS) $(GENCODE) -o $@ $<

clean:
	rm $(TARGET)
