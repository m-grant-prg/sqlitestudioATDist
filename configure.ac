##########################################################################
##									##
## Script ID: ./configure.ac						##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Autoconfigure script file to configure sqlitestudioATDist project.	##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 07/08/2014	MG	1.0.1	Initial version.			##
## 13/08/2014	MG	1.0.2	Changed name to use LUXDist.		##
## 14/08/2014	MG	1.0.3	Changed name to ATDist.			##
## 23/08/2014	MG	1.0.4	Added AC_CANONICAL_HOST statement to	##
##				provide variables to support change to	##
##				an architecture-dependent install.	##
## 29/11/2014	MG	1.0.5	Remove redundant hashpling.		##
## 29/11/2014	MG	1.0.6	Re-structure to cope with OS		##
##				differences. Add check for GNU getopt.	##
## 29/11/2014	MG	1.0.7	Add support for passing overall package	##
##				version to Makefiles.			##
## 27/06/2015	MG	1.0.8	Remove BSD support.			##
##									##
##########################################################################


AC_PREREQ([2.65])
AC_INIT([sqlitestudio AutoTools Distribution], m4_esyscmd([git describe --always 1>/dev/null 2>/dev/null && git describe --always | tr -d '\n' || echo 'Pre-Release' | tr -d '\n']), [m.grant.prg@gmail.com], [sqlitestudioatdist])

AC_SUBST(pkgversion, m4_esyscmd([git describe --always 1>/dev/null 2>/dev/null && git describe --always | tr -d '\n' || echo 'Pre-Release' | tr -d '\n']))

AM_INIT_AUTOMAKE

AC_CONFIG_FILES([Makefile
		src/applications/Makefile
		src/manpages/man1/Makefile
		src/scripts/Makefile
		src/distobjects/Makefile])

AC_CONFIG_MACRO_DIRS([m4])

# Checks for programs.
AC_MSG_NOTICE([checking for required generic programs])
AC_CHECK_PROG(BASH, bash, yes, no)
if test "x$BASH" = "xno" ; then
   	AC_MSG_ERROR([bash not found])
fi

AC_CHECK_PROG(TAR, tar, yes, no)
if test "x$TAR" = "xno" ; then
   	AC_MSG_ERROR([tar not found])
fi

AC_CHECK_PROG(TXT2MAN, txt2man, yes, no)
if test "x$TXT2MAN" = "xno" ; then
   	AC_MSG_ERROR([txt2man not found])
fi

AC_CHECK_PROG(GETOPT, getopt, yes, no)
if test "x$GETOPT" = "xno" ; then
	AC_MSG_ERROR([getopt not found])
fi

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_OUTPUT
