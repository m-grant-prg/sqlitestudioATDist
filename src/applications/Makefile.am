#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/applications/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to generate sqlitestudio.desktop file from	##
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
##									##
##########################################################################



appsrcdir = $(srcdir)
desktopdir = /usr/share/applications

edit = sed \
	-e 's|@bindir[@]|$(bindir)|g' \
	-e 's|@pkgdatadir[@]|$(pkgdatadir)|g' \
	-e 's|@sysconfdir[@]|$(sysconfdir)|g' \
	-e 's|@datadir[@]|$(datadir)|g' \
	-e 's|@prefix[@]|$(prefix)|g'

../../applications/sqlitestudio.desktop: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || appsrcdir=$(appsrcdir)/; \
	$(edit) $${appsrcdir}$(@F).in >$@.tmp

	mv $@.tmp $@

sqlitestudio.desktop: $(appsrcdir)/sqlitestudiodesktop.in

desktop_DATA = ../../applications/sqlitestudio.desktop

EXTRA_DIST = $(appsrcdir)/sqlitestudio.desktop.in
