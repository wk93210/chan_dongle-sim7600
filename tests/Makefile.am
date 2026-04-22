# Tests for chan_dongle

noinst_PROGRAMS = test_at_parse

test_at_parse_SOURCES = test_at_parse.c

test_at_parse_CFLAGS = \
	-O2 -g -Wall -std=gnu11 \
	-D_GNU_SOURCE \
	-I$(top_srcdir) \
	$(SQLITE3_CFLAGS) \
	-I$(ASTERISK_INCLUDE_DIR)

test_at_parse_LDADD = \
	$(top_builddir)/at_parse.o \
	$(top_builddir)/char_conv.o \
	$(top_builddir)/pdu.o \
	$(top_builddir)/memmem.o \
	$(SQLITE3_LIBS)

test_at_parse_LDFLAGS = -lpthread

# Test target
check: test_at_parse
	./test_at_parse

.PHONY: test
test: check
