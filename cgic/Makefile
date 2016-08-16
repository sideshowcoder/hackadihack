.DEFAULT_GOAL:= all

hello_world.cgi: hello_world.c
	cc hello_world.c -o hello_world.cgi

.PHONY: test
test: hello_world.cgi
	./hello_world.cgi

.PHONY: all
all: hello_world.cgi test

.PHONY: clean
clean:
	rm hello_world.cgi
