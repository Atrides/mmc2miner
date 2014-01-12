if WANT_JANSSON
JANSSON_INCLUDES= -I$(top_srcdir)/compat/jansson
else
JANSSON_INCLUDES=
endif

EXTRA_DIST	= example-cfg.json

SUBDIRS		= compat

INCLUDES	= $(PTHREAD_FLAGS) -fno-strict-aliasing $(JANSSON_INCLUDES)

bin_PROGRAMS	= minerd2

minerd2_SOURCES	= elist.h miner.h compat.h cpu-miner.c util.c momentum.cpp
minerd2_LDFLAGS	= $(PTHREAD_FLAGS)
minerd2_LDADD	= @LIBCURL@ @JANSSON_LIBS@ @PTHREAD_LIBS@
minerd2_CPPFLAGS = @LIBCURL_CPPFLAGS@
