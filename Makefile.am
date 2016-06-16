AUTOMAKE_OPTIONS=foreign
EXTRA_DIST=INSTALL.md INSTALL.md.in LICENSE README.md

AM_CFLAGS=-Wall -Wextra -pedantic-errors -Wno-unused-parameter -Werror

bin_PROGRAMS=src/pick
dist_src_pick_SOURCES=src/pick.c src/compat.h src/compat.c
dist_man_MANS=man/man1/pick.1

TESTS=tests/test.sh
check_PROGRAMS=tests/test
tests_test_SOURCES=tests/test.sh tests/test.c
# Required by posix_openpt on Linux.
tests_test_CFLAGS=-D_XOPEN_SOURCE=600

INSTALL.md: INSTALL.md.in
	sed -e 's|@PACKAGE_VERSION[@]|$(PACKAGE_VERSION)|g' $@.in > $@
