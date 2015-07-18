SUBDIRS = src debian

xorgconfdir = $(sysconfdir)/X11/xorg.conf.d/
dist_xorgconf_DATA = 50-ft5x-xorg.conf

deb: dist
	rm -rf dpkg-deb
	mkdir dpkg-deb
	cd dpkg-deb && tar xf ../$(distdir).tar.gz
	cd dpkg-deb/$(distdir) && dpkg-buildpackage -us -uc
