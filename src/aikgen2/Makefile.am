bin_PROGRAMS = aikgen2

aikgen2_SOURCES = aikgen2.c

aikgen2_LDADD = $(top_builddir)/src/libstrongswan/libstrongswan.la
aikgen2.o :	$(top_builddir)/config.status

if USE_TSS2
  aikgen2_LDADD += -ltss2
endif

AM_CPPFLAGS = \
	-I$(top_srcdir)/src/libstrongswan \
	-DIPSEC_CONFDIR=\"${sysconfdir}\" \
	-DPLUGINS=\""${aikgen_plugins}\""
