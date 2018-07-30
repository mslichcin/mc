
noinst_LTLIBRARIES = libmcfilemanager.la

libmcfilemanager_la_SOURCES = \
	achown.cpp achown.h \
	boxes.cpp boxes.h \
	chmod.cpp chmod.h \
	chown.cpp chown.h \
	cmd.cpp cmd.h \
	command.cpp command.h \
	dir.cpp dir.h \
	ext.cpp ext.h \
	file.cpp file.h \
	filegui.cpp filegui.h \
	filenot.cpp filenot.h \
	fileopctx.cpp fileopctx.h \
	find.cpp find.h \
	hotlist.cpp hotlist.h \
	info.cpp info.h \
	ioblksize.h \
	layout.cpp layout.h \
	midnight.h midnight.cpp \
	mountlist.cpp mountlist.h \
	panelize.cpp panelize.h \
	panel.cpp panel.h \
	tree.cpp tree.h \
	treestore.cpp treestore.h

# Unmaintained, unsupported, etc
#	listmode.cpp listmode.h

AM_CPPFLAGS = -I$(top_srcdir) $(GLIB_CFLAGS) $(PCRE_CPPFLAGS)

libmcfilemanager_la_LIBADD = ../../lib/libmc.la
