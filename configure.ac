AC_INIT(gnome-mahjongg, 3.10.2)
AM_INIT_AUTOMAKE([1.11 no-dist-gzip dist-xz foreign])
AM_SILENT_RULES([yes])
AM_MAINTAINER_MODE
GNOME_MAINTAINER_MODE_DEFINES

AM_PROG_VALAC([0.16.0])
AM_PROG_CC_C_O

AC_PATH_PROG(GLIB_COMPILE_RESOURCES, glib-compile-resources)

GLIB_GSETTINGS

dnl ###########################################################################
dnl Dependencies
dnl ###########################################################################

GTK_REQUIRED=3.4.0
RSVG_REQUIRED=2.32.0

PKG_CHECK_MODULES(GNOME_MAHJONGG, [
  gtk+-3.0 >= $GTK_REQUIRED
  librsvg-2.0 >= $RSVG_REQUIRED
])

dnl ###########################################################################
dnl Internationalization
dnl ###########################################################################

IT_PROG_INTLTOOL([0.35.0])
AC_SUBST(GETTEXT_PACKAGE, gnome-mahjongg)

dnl ###########################################################################
dnl Documentation
dnl ###########################################################################

YELP_HELP_INIT

dnl ###########################################################################
dnl Files to generate
dnl ###########################################################################

AC_OUTPUT([
Makefile
po/Makefile.in
data/Makefile
data/icons/Makefile
data/icons/hicolor/Makefile
data/icons/HighContrast/Makefile
data/mahjongg.desktop.in
help/Makefile
src/Makefile
])
