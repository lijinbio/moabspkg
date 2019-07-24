bin_PROGRAMS = mcall

samtools_INCLUDE = $(top_srcdir)/lib/samtools
samtools_LIB = $(top_srcdir)/lib/samtools

mcall_CPPFLAGS = -g -O3 -Wall -w -I$(samtools_INCLUDE)
mcall_LDFLAGS = -L$(samtools_LIB)
mcall_LDADD = -lboost_program_options -lboost_system -lboost_filesystem -lboost_thread -lboost_date_time -lbam -lz -lpthread

mcall_SOURCES =  mcall.cpp
