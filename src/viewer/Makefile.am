
noinst_LTLIBRARIES = libmcviewer.la

libmcviewer_la_SOURCES = \
	actions_cmd.cpp \
	ascii.cpp \
	coord_cache.cpp \
	datasource.cpp \
	dialogs.cpp \
	display.cpp \
	growbuf.cpp \
	hex.cpp \
	inlines.h \
	internal.h \
	lib.cpp \
	mcviewer.cpp \
	mcviewer.h \
	move.cpp \
	nroff.cpp \
	search.cpp

AM_CPPFLAGS = -I$(top_srcdir) $(GLIB_CFLAGS) $(PCRE_CPPFLAGS)

libmcviewer_la_LIBADD = ../../lib/libmc.la
