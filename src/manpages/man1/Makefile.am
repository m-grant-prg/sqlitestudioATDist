#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/manpages/man1/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to generate sqlitestudio manual pages from	##
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


manpagessrcdir = $(srcdir)

../../../manpages/man1/sqlitestudio.1: Makefile
	mkdir -p $(@D)
	rm -f $@
	txt2man -t sqlitestudio -s 1 -v "sqlitestudio Manual" \
		$(manpagessrcdir)/$(@F).txt > $@

sqlitestudio.1: $(manpagessrcdir)/sqlitestudio.1.txt

man1_MANS = ../../../manpages/man1/sqlitestudio.1

EXTRA_DIST = $(manpagessrcdir)/sqlitestudio.1.txt
