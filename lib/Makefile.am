SUBDIRS = event filehighlight mcconfig search skin tty vfs strutil widget .

if ENABLE_MCLIB
    LIB_VERSION=`echo $(LIBMC_VERSION) | \
	tr '.' ' '| \
	while read v1 v2 v3; do echo $$v2':'$$v3':'$$v1; done`

    AM_LDFLAGS=-no-undefined -version-info $(LIB_VERSION) -release $(LIBMC_RELEASE)

    lib_LTLIBRARIES = libmc.la
else
    noinst_LTLIBRARIES = libmc.la
endif


SUBLIB_includes = \
	event.h event-types.h \
	filehighlight.h \
	mcconfig.h \
	search.h \
	skin.h \
	strescape.h \
	strutil.h \
	widget.h

SRC_mc_utils = \
	utilunix.cpp utilunix.h \
	unixcompat.h \
	util.cpp util.h


libmc_la_SOURCES = \
	$(SUBLIB_includes) \
	$(SRC_mc_utils) \
	fileloc.h \
	fs.h \
	hook.cpp hook.h \
	glibcompat.cpp glibcompat.h \
	global.cpp global.h \
	keybind.cpp keybind.h \
	lock.cpp lock.h \
	serialize.cpp serialize.h \
	shell.cpp shell.h \
	stat-size.h \
	timefmt.cpp timefmt.h \
	timer.cpp timer.h

if USE_MAINTAINER_MODE
libmc_la_SOURCES += logging.cpp logging.h
endif

if CHARSET
libmc_la_SOURCES += charsets.cpp charsets.h
endif

AM_CPPFLAGS = $(GLIB_CFLAGS) -I$(top_srcdir)

libmc_la_LIBADD = \
	event/libmcevent.la \
	filehighlight/libmcfilehighlight.la \
	mcconfig/libmcconfig.la \
	search/libsearch.la \
	strutil/libmcstrutil.la \
	skin/libmcskin.la \
	tty/libmctty.la \
	vfs/libmcvfs.la \
	widget/libmcwidget.la

libmc_la_LIBADD += $(MCLIBS) $(SLANGLIB)

if HAVE_GMODULE
    libmc_la_LIBADD += $(GMODULE_LIBS)
else
    libmc_la_LIBADD += $(GLIB_LIBS)
endif

libmc_la_LIBADD += $(PCRE_LIBS) $(LIBICONV) $(LIBINTL)
