# Makefile for cmd/scripts.

CFLAGS	= -D_MINIX -D_POSIX_SOURCE
CCLD	= $(CC) -i $(CFLAGS)
MAKE	= exec make -$(MAKEFLAGS) install

all:		# Does nothing

install:	usr root

# Commands on the /usr partition.
usr:	\
	/usr/bin/DESCRIBE \
	/usr/bin/M \
		/usr/bin/U \
	/usr/bin/MAKEDEV \
	/usr/bin/adduser \
	/usr/bin/checkhier \
	/usr/bin/makewhatis \
	/usr/bin/mkdist \
	/usr/bin/setup \
	/usr/bin/spell \
	/usr/bin/srccrc \
	/usr/bin/svclog \
	/usr/bin/true \
		/usr/bin/false \
	/usr/bin/whatis \
		/usr/bin/apropos \
	/usr/bin/whereis \

# Commands on the root partition.
root:	\
	/bin/M \
		/bin/U \
	/bin/true \
		/bin/false \

clean:

/usr/bin/DESCRIBE:	DESCRIBE.sh
	install -c -o bin $? $@

/usr/bin/M:	M.sh
	install -c -o bin $? $@

/usr/bin/U:	/usr/bin/M
	install -l $? $@

/usr/bin/MAKEDEV:	MAKEDEV.sh
	install -c -o bin $? $@

/usr/bin/adduser:	adduser.sh
	install -c -o bin $? $@

/usr/bin/checkhier:	checkhier.sh
	install -c -o bin $? $@

/usr/bin/makewhatis:	makewhatis.sh
	install -c -o bin $? $@

/usr/bin/mkdist:	mkdist.sh
	install -c -o bin $? $@

/usr/bin/setup:	setup.sh
	install -c -o bin $? $@

/usr/bin/spell:	spell.sh
	install -c -o bin $? $@

/usr/bin/srccrc:	srccrc.sh
	install -c -o bin $? $@

/usr/bin/svclog:	svclog.sh
	install -c -o bin $? $@

/usr/bin/true:	true.sh
	install -c -o bin $? $@

/usr/bin/false:	/usr/bin/true
	install -l $? $@

/usr/bin/whatis:	whatis.sh
	install -c -o bin $? $@

/usr/bin/apropos:	/usr/bin/whatis
	install -l $? $@

/usr/bin/whereis:	whereis.sh
	install -c -o bin $? $@

/bin/M:	/usr/bin/M
	install -c -o bin $? $@

/bin/U:	/bin/M
	install -l $? $@

/bin/true:	/usr/bin/true
	install -c -o bin $? $@

/bin/false:	/bin/true
	install -l $? $@
