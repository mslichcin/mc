
AM_CPPFLAGS = $(GLIB_CFLAGS) -I$(top_srcdir) $(LIBSSH_CFLAGS) $(PCRE_CPPFLAGS)

noinst_LTLIBRARIES = libvfs-sftpfs.la

libvfs_sftpfs_la_SOURCES = \
	config_parser.cpp \
	connection.cpp \
	dir.cpp \
	file.cpp \
	init.cpp init.h \
	internal.cpp internal.h \
	vfs_class.cpp \
	vfs_subclass.cpp
