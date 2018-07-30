DIST_SUBDIRS =

SUBDIRS = helpers

AM_CPPFLAGS = \
	-DCONFIGDIR=\""@smbconfigdir@"\" \
	$(GLIB_CFLAGS) \
	-I$(top_srcdir)

noinst_LTLIBRARIES = libvfs-smbfs.la

libvfs_smbfs_la_SOURCES = \
	smbfs.cpp smbfs.h

SAMBA_DIST =			\
	Makefile.in		\
	aclocal.m4		\
	configure.ac		\
	configure		\
	internals.doc		\
	parsing.doc		\
	include/byteorder.h	\
	include/charset.h	\
	include/client.h	\
	include/config.h.in	\
	include/includes.h	\
	include/kanji.h		\
	include/local.h		\
	include/nameserv.h	\
	include/nterr.h		\
	include/proto.h		\
	include/smb.h		\
	include/stamp-h.in	\
	include/trans2.h	\
	include/version.h	\
	lib/charcnv.cpp		\
	lib/charset.cpp		\
	lib/debug.cpp		\
	lib/interface.cpp		\
	lib/kanji.cpp		\
	lib/md4.cpp		\
	lib/netmask.cpp		\
	lib/slprintf.cpp		\
	lib/system.cpp		\
	lib/time.cpp		\
	lib/username.cpp		\
	lib/util.cpp		\
	lib/util_file.cpp		\
	lib/util_sock.cpp		\
	lib/util_str.cpp		\
	libsmb/clientgen.cpp	\
	libsmb/namequery.cpp	\
	libsmb/nmblib.cpp		\
	libsmb/nterr.cpp		\
	libsmb/pwd_cache.cpp	\
	libsmb/smbdes.cpp		\
	libsmb/smbencrypt.cpp	\
	libsmb/smberr.cpp		\
	param/loadparm.cpp	\
	param/params.cpp

dist-hook:
	$(mkinstalldirs) $(distdir)/helpers
	$(mkinstalldirs) $(distdir)/helpers/include
	$(mkinstalldirs) $(distdir)/helpers/lib
	$(mkinstalldirs) $(distdir)/helpers/libsmb
	$(mkinstalldirs) $(distdir)/helpers/param
	for I in $(SAMBA_DIST); do \
	  cp -p $(srcdir)/helpers/$$I $(distdir)/helpers/$$I || exit 1; \
	done

mostlyclean-local:
	if test -f helpers/Makefile; then \
	  (cd helpers && $(MAKE) mostlyclean) \
	else :; fi

clean-local:
	if test -f helpers/Makefile; then \
	  (cd helpers && $(MAKE) clean) \
	else :; fi

distclean-local:
	if test -f helpers/Makefile; then \
	  (cd helpers && $(MAKE) distclean) \
	else :; fi

