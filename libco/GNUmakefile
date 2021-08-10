libco.objects := libco
libco.objects := $(libco.objects:%=$(object.path)/%.o)

$(object.path)/libco.o: $(libco.path)/libco.c
	# TODO: figure out how to remove -flto -fwhole-program from cflags only here
	# (or fix ppc64v2.c to not have the swap_context symbol dropped by cc lto)
	$(compiler) $(flags) -c $(libco.path)/libco.c -o $(object.path)/libco.o
