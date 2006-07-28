#
# $Id: Makefile,v 1.4 2003/10/05 00:35:34 webbie Exp $
#

CFLAGS += -Wall

INSTALL_PREFIX = /usr/local
INSTALL = /usr/bin/install -c
INSTALL_PROGRAM = ${INSTALL}

STRIP = strip
INDENT = /usr/local/bin/gindent


all: bsdsfv

bsdsfv: bsdsfv.c
	${CC} ${CFLAGS} ${LDFLAGS} $< -o $@
	${STRIP} $@

install:
	${INSTALL_PROGRAM} bsdsfv ${INSTALL_PREFIX}/bin

clean:
	rm -f bsdsfv *.o *.c~ bsdsfv.tar.gz

indent: 
	${INDENT} bsdsfv.c

tarball: clean maketarball

maketarball:
	@cd ..; tar -cnzvf bsdsfv/bsdsfv.tar.gz bsdsfv/*
