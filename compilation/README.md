preprocessor :

main.c -->main.i

commands :
cpp main.c -o main.i
gcc -E main.c -o main.i


Compiler :
 main.i -->main.s 

command :

gcc -S main.i

output :main.s (Assembly)

Assembler:

main.s -->main.o

Command:

gcc -c main.s
as main.s

main.o :Format ELF :Relocatable

Linker:

main.o -->Executable 

command :

gcc file.c main.o -o main
 
main:Executable


