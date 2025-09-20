CC=$(CROSS_COMPILE)gcc
#or CC=$(TOOLCHAIN_PREFIX)gcc
EXEC=main
LIB=libfile.so
$(EXEC): main.o libfile.so
	@echo "creating executable $(EXEC) "
	@$(CC) main.o -lfile -L$(shell pwd) -o  $(EXEC)

main.o: main.c
	@$(CC) -c main.c

$(LIB): file.o
	@echo "creating $(LIB) "
	@$(CC) file.o -shared -fPIC -Wl,-soname,libfile.so.1 -o libfile.so.1.0
	@ln -s libfile.so.1.0 libfile.so.1
	@ln -s libfile.so.1 $(LIB)

file.o: file.c
	@$(CC) -c file.c


clean:
	@echo "cleaning"
	@rm -f  *.o $(EXEC) $(LIB)*
