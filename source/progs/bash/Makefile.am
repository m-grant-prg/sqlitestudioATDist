#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/progs/bash/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to generate sqlitestudio script from source.	##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 07/08/2014	MG	1.0.1	Started versioning of this script.	##
## 29/11/2014	MG	1.0.2	Add script substitution variable for	##
##				overall package version.		##
## 20/10/2015	MG	1.0.3	Restructure to conform to AutoTools	##
##				General Template v1.0.5.		##
##									##
##########################################################################


sqlitestudio: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@

sqlitestudio: $(srcdir)/sqlitestudio.in

bin_SCRIPTS = sqlitestudio

EXTRA_DIST = $(srcdir)/sqlitestudio.in

CLEANFILES = *.tmp sqlitestudio

