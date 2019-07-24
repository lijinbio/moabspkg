bin_PROGRAMS = mcomp

samtools_INCLUDE = $(top_srcdir)/lib/samtools
samtools_LIB = $(top_srcdir)/lib/samtools

mcomp_CPPFLAGS = -O3 -pipe -Wall -w -Ilib -isystem -Ilib/eigen_3.2.4 -DBOOST_RESULT_OF_USE_TR1 -DBOOST_NO_DECLTYPE -DBOOST_DISABLE_ASSERTS -Wno-unused-function
mcomp_LDADD = -lboost_program_options -lboost_system -lboost_filesystem -lboost_thread -lpthread

mcomp_SOURCES = \
	Boolean.h \
	Constants.h \
	Memory.h \
	bbf.h bbf.cpp \
	fet2x2.h fet2x2.cpp \
	fexact.h fexact.c \
	fisher_exact_test.h fisher_exact_test.cpp \
	hmm.h hmm.cpp \
	lut.h lut.cpp \
	stats.h stats.cpp \
	types.h types.cpp \
	mcomp.cpp
