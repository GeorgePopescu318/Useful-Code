# *Makefile*
## What are Makefiles?
Makefiles are a sort of shortcut that you can use while working with shell commands.
## How to create one?
You just have to create a new file with the name `Makefile` and that's it!
## Okay and what next?
Now you will create the actual shortcuts. For example to write *"Hello, World!"* in the terminal you could use:
>       say_hello:   
>               echo "Hello, world!"
In this instance the `say_hello` is called the *target* this represents the shortcut, the way we are going to actually call the command written bellow, `echo "Hello, world!"` that is called the *target*, in the terminal.

And then you will call the command like this:
>       make say_hello
And the output will be:
>       Hello, world!
## The way I use them is mostly for calling the gcc compiler :)
>       compile: build run
>       valgrind: build valgrind
>       build: [c file name*]
>	         gcc [c file name] -Wall -g -o compiler
>       run: [compiler name**]
>	        ./ [compiler name]
>       valgrind:  [compiler name]
>	            valgrind -v --leak-check=full --show-leak-kinds=all >--track-origins=yes --vgdb=full --error-exitcode=1 ./ [compiler name]
### Okay that could be a little more than the say_hello command but I will explain all of the abomination from above:
- 


**Work in progress**