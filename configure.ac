AC_PREREQ(2.52)

AC_INIT([Apertium Central Puebla Nahuatl], [0.1.0], [https://github.com/apertium/apertium-ncx/issues], [apertium-ncx], [https://wiki.apertium.org/wiki/Apertium-ncx])
AM_INIT_AUTOMAKE
AC_PROG_AWK

PKG_CHECK_MODULES(LTTOOLBOX, lttoolbox >= 3.5.2)
PKG_CHECK_MODULES(APERTIUM, apertium >= 3.6.3)
PKG_CHECK_MODULES(HFST, hfst >= 3.15.2)
PKG_CHECK_MODULES(CG3, cg3 >= 1.3.6)

PKG_CHECK_MODULES(HFSTOSPELL, hfstospell >= 0.5.3, [], [
      AC_MSG_NOTICE([You will need hfst-ospell installed to use the compiled speller])
])

PKG_CHECK_MODULES(REGTEST, apertium-regtest >= 0.9.1, [],
                  [AC_MSG_WARN([Running tests requires apertium-regtest])])

AP_MKINCLUDE

AC_CONFIG_FILES([Makefile apertium-ncx.pc])
AC_OUTPUT
