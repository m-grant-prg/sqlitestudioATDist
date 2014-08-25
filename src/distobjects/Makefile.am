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
## 23/08/2014	MG	1.0.2	Added support for architecture-		##
##				dependent external binaries.		##
## 25/08/2014	MG	1.0.3	Reverted to use the upstream binary	##
##				.bin extension.				##
##									##
##########################################################################


distobjectssrcdir = $(srcdir)
pkgfilesdir = $(pkgdatadir)
pkgappsdir = $(pkglibexecdir)

../../distobjects/Share/sqlitestudio.bin: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	mv $(host_cpu)/sqlitestudio*.tar.gz .
	./extdisttar
	cp $(distobjectssrcdir)/$(@F) $@
	chmod a+x $@

sqlitestudio.bin: $(distobjectssrcdir)/sqlitestudio.bin

../../distobjects/Share/sqlitestudio.png: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	cp $(distobjectssrcdir)/$(@F).in $@

sqlitestudio.png: $(distobjectssrcdir)/sqlitestudio.png.in

pkgfiles_DATA = ../../distobjects/Share/sqlitestudio.png
pkgapps_SCRIPTS = ../../distobjects/Share/sqlitestudio.bin

EXTRA_DIST = $(distobjectssrcdir)/i386 $(distobjectssrcdir)/x86_64 \
	$(distobjectssrcdir)/extdisttar $(distobjectssrcdir)/sqlitestudio.png.in
