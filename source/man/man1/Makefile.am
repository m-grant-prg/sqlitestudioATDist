#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/man/man1/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to generate sqlitestudio manual pages from	##
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
## 30/10/2016	MG	1.1.0	Add build of sqlitestudiocli man page.	##
##									##
##########################################################################


sqlitestudio.1 sqlitestudiocli.1: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).txt > $@.tmp
	mv $@.tmp $@
	txt2manwrap $(@F) 1 "sqlitestudio Manual" $(srcdir)/$(@F).txt $@
	rm -f $@.tmp

sqlitestudio.1: $(srcdir)/sqlitestudio.1.txt
sqlitestudiocli.1: $(srcdir)/sqlitestudiocli.1.txt

man_MANS = sqlitestudio.1 sqlitestudiocli.1

EXTRA_DIST = $(srcdir)/sqlitestudio.1.txt $(srcdir)/sqlitestudiocli.1.txt

CLEANFILES = *.tmp sqlitestudio.1 sqlitestudiocli.1

