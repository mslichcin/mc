noinst_LTLIBRARIES = libmcvfs.la

AM_CPPFLAGS = $(GLIB_CFLAGS) -I$(top_srcdir)

libmcvfs_la_SOURCES = \
	direntry.cpp		\
	gc.cpp gc.h		\
	interface.cpp \
	parse_ls_vga.cpp \
	path.cpp path.h		\
	vfs.cpp vfs.h		\
	utilvfs.cpp utilvfs.h	\
	xdirentry.h

if ENABLE_VFS_NET
libmcvfs_la_SOURCES += netutil.cpp netutil.h
endif

EXTRA_DIST = HACKING README
