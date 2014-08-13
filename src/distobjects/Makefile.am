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
appfilesdir = $(datadir)/sqlitestudio

../../distobjects/Share/sqlitestudio.bin: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	./extdisttar
	cp $(distobjectssrcdir)/$(@F) $@
	chmod a+x $@

sqlitestudio.bin: $(distobjectssrcdir)/sqlitestudio.bin

../../distobjects/Share/sqlitestudio.png: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	cp $(distobjectssrcdir)/$(@F).in $@

sqlitestudio.png: $(distobjectssrcdir)/sqlitestudio.png.in

appfiles_DATA = ../../distobjects/Share/sqlitestudio.png ../../distobjects/Share/sqlitestudio.bin

EXTRA_DIST = $(distobjectssrcdir)/sqlitestudio*.tar.gz $(distobjectssrcdir)/extdisttar \
		$(distobjectssrcdir)/sqlitestudio.png.in $(distobjectssrcdir)/sqlitestudio.bin
