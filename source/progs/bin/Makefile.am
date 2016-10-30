#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/progs/bin/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to install sqlitestudio project.		##
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
## 30/10/2016	MG	1.1.0	Change to accommodate new upstream	##
##				package format, (directories,		##
##				executables, etc.			##
##									##
##########################################################################


$(host_cpu)/sqlitestudio*.tar.*: Makefile


SQLiteStudio/sqlitestudio: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	tar xvpf $(srcdir)/$(host_cpu)/sqlitestudio*.tar.*
SQLiteStudio/sqlitestudio: $(host_cpu)/sqlitestudio*.tar.*


SQLiteStudio/sqlitestudiocli: Makefile
SQLiteStudio/sqlitestudiocli: $(host_cpu)/sqlitestudio*.tar.*


## Install accompanying files
install-data-local:
	$(MKDIR_P) $(DESTDIR)$(pkglibexecdir)/iconengines
	$(MKDIR_P) $(DESTDIR)$(pkglibexecdir)/imageformats
	$(MKDIR_P) $(DESTDIR)$(pkglibexecdir)/lib
	$(MKDIR_P) $(DESTDIR)$(pkglibexecdir)/platforms
	$(MKDIR_P) $(DESTDIR)$(pkglibexecdir)/plugins
	$(MKDIR_P) $(DESTDIR)$(pkglibexecdir)/printsupport

	$(INSTALL_DATA) SQLiteStudio/iconengines/* \
			$(DESTDIR)$(pkglibexecdir)/iconengines
	$(INSTALL_DATA) SQLiteStudio/imageformats/* \
			$(DESTDIR)$(pkglibexecdir)/imageformats
	$(INSTALL_DATA) SQLiteStudio/lib/* \
			$(DESTDIR)$(pkglibexecdir)/lib
	$(INSTALL_DATA) SQLiteStudio/platforms/* \
			$(DESTDIR)$(pkglibexecdir)/platforms
	$(INSTALL_DATA) SQLiteStudio/plugins/* \
			$(DESTDIR)$(pkglibexecdir)/plugins
	$(INSTALL_DATA) SQLiteStudio/printsupport/* \
			$(DESTDIR)$(pkglibexecdir)/printsupport


## Uninstall accompanying files
uninstall-local:
	@$(NORMAL_UNINSTALL)
	rm -rf $(DESTDIR)$(pkglibexecdir)


clean-local:
	rm -rf SQLiteStudio


pkglibexec_SCRIPTS = SQLiteStudio/sqlitestudio SQLiteStudio/sqlitestudiocli


EXTRA_DIST = $(srcdir)/i386 $(srcdir)/x86_64


CLEANFILES = SQLiteStudio/*.tmp SQLiteStudio/sqlitestudio \
		SQLiteStudio/sqlitestudiocli
