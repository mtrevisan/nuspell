lib_LTLIBRARIES = libnuspell.la

AM_CPPFLAGS = $(BOOST_CPPFLAGS)   $(CODE_COVERAGE_CPPFLAGS)
AM_CXXFLAGS = -std=c++14          $(CODE_COVERAGE_CXXFLAGS)
AM_LDFLAGS  = $(BOOST_LOCALE_LDFLAGS)
libnuspell_la_LIBADD=$(BOOST_LOCALE_LIBS) $(ICU_LIBS) $(CODE_COVERAGE_LIBS)

libnuspell_la_SOURCES=\
aff_data.cxx     aff_data.hxx     \
condition.cxx    condition.hxx    \
dictionary.cxx   dictionary.hxx   \
finder.cxx       finder.hxx       \
locale_utils.cxx locale_utils.hxx \
                 string_utils.hxx \
structures.cxx   structures.hxx

pkginclude_HEADERS=\
aff_data.hxx     \
condition.hxx    \
dictionary.hxx   \
finder.hxx       \
locale_utils.hxx \
string_utils.hxx \
structures.hxx

bin_PROGRAMS = nuspell
nuspell_SOURCES = main.cxx
LDADD = libnuspell.la $(BOOST_LOCALE_LIBS) $(CODE_COVERAGE_LIBS)
