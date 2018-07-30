PACKAGE_STRING = "/lib/vfs"

AM_CPPFLAGS = \
	-DTEST_SHARE_DIR=\"$(abs_srcdir)\" \
	$(GLIB_CFLAGS) \
	-I$(top_srcdir) \
	-I$(top_srcdir)/lib/vfs \
	@CHECK_CFLAGS@

AM_LDFLAGS = @TESTS_LDFLAGS@

EXTRA_DIST = mc.charsets

LIBS = @CHECK_LIBS@ \
	$(top_builddir)/lib/libmc.la

if ENABLE_MCLIB
LIBS += $(GLIB_LIBS)
endif

TESTS = \
	canonicalize_pathname \
	current_dir \
	path_cmp \
	path_len \
	path_manipulations \
	path_serialize \
	relative_cd \
	tempdir \
	vfs_adjust_stat \
	vfs_parse_ls_lga \
	vfs_path_from_str_flags \
	vfs_path_string_convert \
	vfs_prefix_to_class \
	vfs_setup_cwd \
	vfs_split \
	vfs_s_get_path

if CHARSET
TESTS += path_recode \
	vfs_get_encoding
endif

check_PROGRAMS = $(TESTS)

canonicalize_pathname_SOURCES = \
	canonicalize_pathname.cpp

current_dir_SOURCES = \
	current_dir.cpp

path_cmp_SOURCES = \
	path_cmp.cpp

path_len_SOURCES = \
	path_len.cpp

path_manipulations_SOURCES = \
	path_manipulations.cpp

path_recode_SOURCES = \
	path_recode.cpp

path_serialize_SOURCES = \
	path_serialize.cpp

relative_cd_SOURCES = \
	relative_cd.cpp

tempdir_SOURCES = \
	tempdir.cpp

vfs_adjust_stat_SOURCES = \
	vfs_adjust_stat.cpp

vfs_get_encoding_SOURCES = \
	vfs_get_encoding.cpp

vfs_setup_cwd_SOURCES = \
	vfs_setup_cwd.cpp

vfs_split_SOURCES = \
	vfs_split.cpp

vfs_parse_ls_lga_SOURCES = \
	vfs_parse_ls_lga.cpp

vfs_prefix_to_class_SOURCES = \
	vfs_prefix_to_class.cpp

vfs_path_from_str_flags_SOURCES = \
	vfs_path_from_str_flags.cpp

vfs_path_string_convert_SOURCES = \
	vfs_path_string_convert.cpp

vfs_s_get_path_SOURCES = \
	vfs_s_get_path.cpp
