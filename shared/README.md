create shared object :

gcc file.o -shared libfile.so
gcc -->linker 

dynamic linking :

Now link between them :
gcc main.o -lfile -L$(pwd) -o main


we will find the functions undefined .

'''bash 
ldd main
	linux-vdso.so.1 (0x00007ffd33dc7000)
	libfile.so => not found
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x000074b76b200000)
	/lib64/ld-linux-x86-64.so.2 (0x000074b76b469000)

'''

