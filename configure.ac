AC_PREREQ([2.69])
AC_INIT([sidreloc], [1.0], [linus@linusakesson.net], , [http://www.linusakesson.net/software/sidreloc])
AM_INIT_AUTOMAKE

AC_CONFIG_SRCDIR([src/cpu.c])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lm':
AC_CHECK_LIB([m], [main])

# Checks for header files.
AC_CHECK_HEADERS([stdint.h stdlib.h string.h err.h])

AC_DEFINE_UNQUOTED([RELEASE], ["$PACKAGE_VERSION"], [convenience define used for release number])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_INT8_T
AC_TYPE_UINT16_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_CHECK_FUNCS([memset err errx])

AC_CONFIG_FILES([Makefile src/Makefile])
AC_OUTPUT

echo \
"-------------------------------------------------

${PACKAGE_NAME} Version ${PACKAGE_VERSION}

Prefix: '${prefix}'.
Compiler: '${CC} ${CFLAGS} ${CPPFLAGS}'

Now type 'make @<:@<target>@:>@'
   where the optional <target> is:
     all                - build all binaries
     install            - install everything

--------------------------------------------------"
