CC      = gcc
CXX     = g++
CFLAGS  = -g -O3 -Wall -std=c++0x -pthread
LIBS    = -lm -lpthread
LDFLAGS = -g

OBJECTS = APRSWriterThread.o APRSWriter.o Conf.o CRC.o DTMF.o Golay24128.o GPS.o Log.o Network.o Reflectors.o StopWatch.o Sync.o TCPSocket.o Thread.o Timer.o \
					UDPSocket.o Utils.o WiresX.o YSFConvolution.o YSFFICH.o YSFGateway.o YSFPayload.o

all:		YSFGateway

YSFGateway:	$(OBJECTS)
		$(CXX) $(OBJECTS) $(CFLAGS) $(LIBS) -o YSFGateway

%.o: %.cpp
		$(CXX) $(CFLAGS) -c -o $@ $<

clean:
		$(RM) YSFGateway *.o *.d *.bak *~
 