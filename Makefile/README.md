# *Makefile*
## What are Makefiles?
Makefiles are a sort of shortcut that you can use while working with shell commands.
## How to create one?
You just have to create a new file with the name `Makefile` and that's it!
## Okay and what next?
Now you will create the actual shortcuts. For example to write *"Hello, World!"* in the terminal you could use:
>       say_hello:   
>               echo "Hello, world!"
In this instance the `say_hello` is called the *target* this represents the shortcut, the way we are going to actually call the command written bellow, `echo "Hello, world!"` that is called the *recipe*, in the terminal.

And then you will call the command like this:
>       make say_hello
And the output will be:
>       Hello, world!
## The way I use them is mostly for calling the gcc compiler :)
>       compile: build run
>       valgrind: build valgrind
>       build: [c file name]
>	         gcc [c file name] -Wall -g -o [compiler name]
>       run: [compiler name]
>	        ./ [compiler name]
>       valgrind:  [compiler name]
>	            valgrind -v --leak-check=full --show-leak-kinds=all >--track-origins=yes --vgdb=full --error-exitcode=1 ./ [compiler name]
## Okay that could be a little more than the say_hello command but I will explain all of the abomination from above:
- ### First of all I will talk about the build command:
  >      ​build: [c file name*]
  >           ​gcc [c file name] -Wall -g -o [compiler name]
The [c file name] stands for the name of your C (in my chase) file with the .c extension. `build` will be the *target*, the label, next to it we will add the name of the C file again so that the command knows which file to call. Bellow is the shell command for the C compiler: 
> `gcc` *(C compiler)* [c file name] `-Wall` *(Warnings all)* `-g` *(with -g we'll be able to see the row of the error when using valgrind)* `-o` *(without this the compiler will be created with the name `f.out`, so with it we are renaming it to->)* [compiler name]
- ### The run command:
>     ​run: [compiler name]
>        ​./ [compiler name]
The [compiler name] stands for the name of the compiler you declared above *(again without the -o command the default compiler name will be a.out)* 






**Work in progress**