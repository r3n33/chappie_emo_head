###############################################################
#
# Purpose: Makefile for "emo_head_demo"
# Author.: robotis
# Version: 0.1
# License: GPL
#
###############################################################

TARGET = emo_head_demo

CXX = g++
INCLUDE_DIRS = -I../../include -I../../../Framework/include
CXXFLAGS += -fPIC -O2 -DLINUX -g -Wall -fmessage-length=0 $(INCLUDE_DIRS)
LIBS += -lpthread -lncurses -lrt -lbluetooth

OBJS =	./main.o


all: darwin.a $(TARGET)

darwin.a:
	make -C ../../build

$(TARGET): $(OBJS) ../../lib/darwin.a
	$(CXX) -o $(TARGET) $(OBJS) ../../lib/darwin.a $(LIBS)
	
clean:
	rm -f $(OBJS) $(TARGET)





