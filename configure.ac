AC_PREREQ([2.57])
AC_INIT(xorg-cf-files, [1.0.2], [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg], xorg-cf-files)
AM_INIT_AUTOMAKE([foreign dist-bzip2])
AM_MAINTAINER_MODE

# Require xorg-macros: XORG_RELEASE_VERSION XORG_CHANGELOG
m4_ifndef([XORG_MACROS_VERSION], [AC_FATAL([must install xorg-macros 1.2 or later before running autoconf/autogen])])
XORG_MACROS_VERSION(1.2)

m4_ifdef([AS_HELP_STRING], , [m4_define([AS_HELP_STRING], m4_defn([AC_HELP_STRING]))])

DEFAULT_XCONFDIR="${libdir}/X11/config"
AC_ARG_WITH(config-dir,
	AS_HELP_STRING([--with-config-dir=<path>], [Path to config dir (default: ${libdir}/X11/config)]),
	[XCONFDIR="$withval"],
	[XCONFDIR="$DEFAULT_XCONFDIR"])
AC_SUBST(XCONFDIR)

XORG_RELEASE_VERSION
XORG_CHANGELOG

AC_OUTPUT([
	Makefile
	site.def
])
