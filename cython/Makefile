
CC= gcc
SAMPLE=sample.pyx
LIBS= `pkg-config --cflags --libs python3`
TARGET=hello
SOURCE= \
hello.c \
sample.c



all: clean compile install

clean:
	rm ./sample.c
	rm ./sample.h
	

compile:
	cython ./$(SAMPLE)
	$(CC) $(SOURCE) $(LIBS) -o ./$(TARGET)

install:
	cp ./$(TARGET) /usr/local/bin/

