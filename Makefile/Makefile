compile: build run
valgrind: build valgrind
build: .......
	 gcc ........ -Wall -g -o compiler
run: compiler
	./compiler
valgrind: compiler
	 valgrind -v --leak-check=full --show-leak-kinds=all --track-origins=yes --vgdb=full --error-exitcode=1 ./compiler

