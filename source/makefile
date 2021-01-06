flags=-g0 -O0 -pthread
compiler=/opt/mipsel-linux-uclibc/usr/bin/mipsel-buildroot-linux-uclibc-g++
linker=/opt/mipsel-linux-uclibc/usr/bin/mipsel-buildroot-linux-uclibc-ar

library:
	@$(compiler) -c retrogdk.cpp $(flags) -o retrogdk.o
	@$(linker) -r retrogdk.a retrogdk.o
	@rm *.o
demo:
	@$(compiler) demo.cpp retrogdk.a $(flags) -o demo
tileset:
	@$(compiler) tileset.cpp retrogdk.a $(flags) -o tileset
full:
	@make library
	@make demo
	@make tileset