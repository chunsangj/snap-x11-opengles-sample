inc=-I.
libs=-lGLESv2 -lEGL -lm -lX11

es2tri=./es2tri.c

default: all

all: ./test_es2tri

clean:
	find . -name "test_*" | xargs rm -f

./test_es2tri: ${es2tri}
	gcc ${es2tri} -o ./$@ ${inc} ${libs}

install:
	install -d -m755 $(DESTDIR)/bin/
	install -m755 ./test_es2tri $(DESTDIR)/bin/test_es2tri
