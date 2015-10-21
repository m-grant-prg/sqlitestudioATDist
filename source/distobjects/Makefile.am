#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/distobjects/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to install sqlitestudio icon.			##
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
## 20/10/2015	MG	1.0.4	Restructure to conform to AutoTools	##
##				General Template v1.0.5.		##
##									##
##########################################################################


sqlitestudio.png: Makefile
	mkdir -p $(@D)
	rm -f $(@)
	cp $(srcdir)/$(@F).in $@

sqlitestudio.png: $(srcdir)/sqlitestudio.png.in

pkgdata_DATA = sqlitestudio.png

EXTRA_DIST = $(srcdir)/sqlitestudio.png.in

CLEANFILES = *.tmp sqlitestudio.png

