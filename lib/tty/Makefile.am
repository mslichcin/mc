
noinst_LTLIBRARIES = libmctty.la

if USE_SCREEN_SLANG
    TTY_SCREEN_SRC = \
	color-slang.cpp color-slang.h \
	tty-slang.cpp tty-slang.h
else
    TTY_SCREEN_SRC = \
	color-ncurses.cpp \
	tty-ncurses.cpp tty-ncurses.h
endif

TTY_SRC = \
	color-internal.cpp color-internal.h \
	color.cpp color.h \
	key.cpp key.h keyxdef.cpp \
	mouse.cpp mouse.h \
	tty.cpp tty.h tty-internal.h \
	win.cpp win.h

if HAVE_TEXTMODE_X11_SUPPORT
TTY_SRC += x11conn.cpp x11conn.h
endif

libmctty_la_SOURCES = $(TTY_SRC) $(TTY_SCREEN_SRC)

AM_CPPFLAGS = -I$(top_srcdir)

if HAVE_GMODULE
AM_CPPFLAGS += $(GMODULE_CFLAGS)
else
AM_CPPFLAGS += $(GLIB_CFLAGS)
endif

