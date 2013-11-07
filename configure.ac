dnl -*- Mode: autoconf -*-
dnl Process this file with autoconf to produce a configure script.
AC_PREREQ(2.53)
AC_INIT(mate-menu-editor, 1.7.0, http://www.mate-desktop.org)
AC_CONFIG_SRCDIR(mozo.in)
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE([1.7 dist-xz no-dist-gzip])
AM_MAINTAINER_MODE

dnl put the ACLOCAL flags in the makefile
ACLOCAL="$ACLOCAL $ACLOCAL_FLAGS"


GETTEXT_PACKAGE=mozo
AC_SUBST(GETTEXT_PACKAGE)
AC_DEFINE_UNQUOTED(GETTEXT_PACKAGE, "$GETTEXT_PACKAGE", [Gettext package])
AM_GLIB_GNU_GETTEXT
IT_PROG_INTLTOOL([0.40.0])

AM_PATH_PYTHON_VERSION(2.7, 2.7.0, 2.6, 2.6.0, 2.5, 2.5.0, 2.4, 2.4.0)

PKG_CHECK_MODULES(MOZO, libmate-menu >= 1.1.0 pygobject-3.0)

AC_CONFIG_FILES([
        Makefile
        po/Makefile.in
        Mozo/Makefile
        data/mozo.desktop.in
	data/Makefile
	data/icons/Makefile
        ])

AC_OUTPUT

