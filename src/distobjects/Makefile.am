#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/distobjects/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to install sqlitestudio and icon.		##
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


distobjectssrcdir = $(srcdir)
pkgfilesdir = $(pkgdatadir)

../../distobjects/Share/sqlitestudio: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	./extdisttar
	cp $(distobjectssrcdir)/$(@F) $@
	chmod a+x $@

sqlitestudio: $(distobjectssrcdir)/sqlitestudio

../../distobjects/Share/sqlitestudio.png: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	cp $(distobjectssrcdir)/$(@F).in $@

sqlitestudio.png: $(distobjectssrcdir)/sqlitestudio.png.in

pkgdata_DATA = ../../distobjects/Share/sqlitestudio.png
pkgdata_SCRIPTS = ../../distobjects/Share/sqlitestudio

EXTRA_DIST = $(distobjectssrcdir)/sqlitestudio*.tar.gz $(distobjectssrcdir)/extdisttar \
		$(distobjectssrcdir)/sqlitestudio.png.in
