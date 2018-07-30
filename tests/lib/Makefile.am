PACKAGE_STRING = "/lib"

SUBDIRS = . mcconfig search strutil vfs widget

AM_CPPFLAGS = $(GLIB_CFLAGS) -I$(top_srcdir) @CHECK_CFLAGS@

AM_LDFLAGS = @TESTS_LDFLAGS@

LIBS = @CHECK_LIBS@ \
	$(top_builddir)/lib/libmc.la

if ENABLE_MCLIB
LIBS += $(GLIB_LIBS)
endif

EXTRA_DIST = utilunix__my_system-common.cpp

TESTS = \
	library_independ \
	mc_build_filename \
	name_quote \
	serialize \
	utilunix__my_system_fork_fail \
	utilunix__my_system_fork_child_shell \
	utilunix__my_system_fork_child \
	x_basename

if CHARSET
TESTS += mc_realpath
endif

check_PROGRAMS = $(TESTS)

library_independ_SOURCES = \
	library_independ.cpp

mc_build_filename_SOURCES = \
	mc_build_filename.cpp

mc_realpath_SOURCES = \
	mc_realpath.cpp

name_quote_SOURCES = \
	name_quote.cpp

serialize_SOURCES = \
	serialize.cpp

utilunix__my_system_fork_fail_SOURCES = \
	utilunix__my_system-fork_fail.cpp

utilunix__my_system_fork_child_shell_SOURCES = \
	utilunix__my_system-fork_child_shell.cpp

utilunix__my_system_fork_child_SOURCES = \
	utilunix__my_system-fork_child.cpp

x_basename_SOURCES = \
	x_basename.cpp

