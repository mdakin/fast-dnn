LIBRARY := libfast-dnn.so
PROJECT_HOME := ../..
OBJFILES := dnn.o jni_dnn.o float_dnn.o
JNI_HEADERS :=../../include/
INCLUDES := -I$(JNI_HEADERS)
CXXFLAGS := $(INCLUDES) -g -O2 -march=native -mtune=native -std=c++11 -funroll-loops -msse4 -fPIC

$(LIBRARY): $(OBJFILES)
	$(CXX) -shared -o $@ $^
	cp $@ $(PROJECT_HOME)/src/java/resources
