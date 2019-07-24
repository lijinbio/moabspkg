AC_PREREQ([2.69])
AC_INIT([moabs], [1.3.4], [dsun@tamu.edu])
AM_INIT_AUTOMAKE()
AC_CONFIG_SRCDIR([src/bsmap/main.cpp])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC
AC_PROG_RANLIB

# Check home directories for external libraries
AC_ARG_WITH(boost, AS_HELP_STRING([--with-boost], [home directory for boost]), BOOST_HOME=$withval, BOOST_HOME=)
AC_ARG_WITH(zlib, AS_HELP_STRING([--with-zlib], [home directory for zlib]), ZLIB_HOME=$withval, ZLIB_HOME=)

# Assign CXXFLAGS
AS_IF([test "x$BOOST_HOME" != "x"], [AC_SUBST([CXXFLAGS], ["-I$BOOST_HOME $CXXFLAGS"]), AC_SUBST([LDFLAGS], ["-L$BOOST_HOME/lib $LDFLAGS"])], [])

# Checks for header files.
AC_CHECK_HEADERS([stdint.h])

AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_INT32_T
AC_TYPE_INT64_T
AC_TYPE_UINT32_T

AC_CONFIG_FILES([
	Makefile
	lib/Makefile
	src/Makefile
	src/bsmap/Makefile
	src/ExactNumCI/Makefile
	src/mcall/Makefile
	src/mcomp/Makefile
	])
AC_OUTPUT
