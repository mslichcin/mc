EXTRA_DIST =

if USE_INTERNAL_EDIT
noinst_LTLIBRARIES = libedit.la
else
noinst_LTLIBRARIES =
endif

libedit_la_SOURCES = \
	bookmark.cpp \
	choosesyntax.cpp \
	edit-impl.h \
	edit.cpp edit.h \
	editbuffer.cpp editbuffer.h \
	editcmd.cpp \
	editcmd_dialogs.cpp editcmd_dialogs.h \
	editdraw.cpp \
	editmenu.cpp \
	editoptions.cpp \
	editwidget.cpp editwidget.h \
	etags.cpp etags.h \
	format.cpp \
	syntax.cpp

if USE_ASPELL
if HAVE_GMODULE
libedit_la_SOURCES += \
	spell.cpp spell.h \
	spell_dialogs.cpp spell_dialogs.h
endif
endif

AM_CPPFLAGS = $(GLIB_CFLAGS) -I$(top_srcdir) $(PCRE_CPPFLAGS)
