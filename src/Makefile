inc=-I.
libs=-lGLESv2 -lEGL -lm -lX11

es2info=./es2info.c
es2tri=./es2tri.c
es2gears=./eglut_x11.c ./eglut.c ./es2gears.c

default: all

all: ./test_es2info ./test_es2tri ./test_es2gears

clean:
	find . -name "test_*" | xargs rm -f

./test_es2info: ${es2info}
	gcc ${es2info} -o ./$@ ${inc} ${libs}
./test_es2tri: ${es2tri}
	gcc ${es2tri} -o ./$@ ${inc} ${libs}
./test_es2gears: ${es2gears}
	gcc ${es2gears} -o ./$@ ${inc} ${libs}

install:
	install -d -m755 $(DESTDIR)/bin/
	install -m755 ./test_es2info $(DESTDIR)/bin/test_es2info
	install -m755 ./test_es2tri $(DESTDIR)/bin/test_es2tri
	install -m755 ./test_es2gears $(DESTDIR)/bin/test_es2gears
