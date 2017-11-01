SUBDIRS = include lib main data po tools

ACLOCAL_AMFLAGS = -I m4

installdir = $(pkglibdir)/python
install_PYTHON = upgrade.py \
	Navigation.pyo NavigationInstance.pyo RecordTimer.pyo PowerTimer.py ServiceReference.pyo \
	keyids.pyo keymapparser.pyo mytest.py skin.pyo timer.pyo GlobalActions.pyo \
	e2reactor.pyo pyo_patcher.py BoxBrandingTest.py

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = enigma2.pc

metadir = $(datadir)/meta
meta_DATA = index-enigma2.xml
CLEANFILES = index-enigma2.xml

EXTRA_DIST = lamedb

index-enigma2.xml: $(top_srcdir)/tools/genmetaindex.py $(top_srcdir)/lib/python/Plugins/*/*/meta/plugin_*.xml
	$(AM_V_GEN)$(PYTHON) $^ > $@
