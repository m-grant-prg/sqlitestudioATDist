#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/desktop/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to generate sqlitestudio.desktop file from	##
## source.								##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 07/08/2014	MG	1.0.1	Started versioning of this script.	##
## 20/10/2015	MG	1.0.2	Restructure to conform to AutoTools	##
##				General Template v1.0.5.		##
##									##
##########################################################################


# desktoploc is set in configure.ac to provide a conditional target depending
# on whether distcheck is being run.
desktopdir = $(desktoploc)

sqlitestudio.desktop: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@

sqlitestudio.desktop: $(srcdir)/sqlitestudio.desktop.in

desktop_DATA = sqlitestudio.desktop

EXTRA_DIST = $(srcdir)/sqlitestudio.desktop.in

CLEANFILES = *.tmp sqlitestudio.desktop

