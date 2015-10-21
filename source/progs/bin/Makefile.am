#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/progs/bin/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to install sqlitestudio.bin.			##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 20/10/2015	MG	1.0.1	Started versioning of this script at	##
##				level of AutoTools General Template	##
##				v1.0.5.					##
##									##
##########################################################################


$(host_cpu)/sqlitestudio*.tar.gz: Makefile

sqlitestudio.bin: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	tar xvpf $(srcdir)/$(host_cpu)/sqlitestudio*.tar.gz
	chmod a+x $@
sqlitestudio.bin: $(host_cpu)/sqlitestudio*.tar.gz

pkglibexec_SCRIPTS = sqlitestudio.bin

EXTRA_DIST = $(srcdir)/i386 $(srcdir)/x86_64

CLEANFILES = *.tmp sqlitestudio.bin

