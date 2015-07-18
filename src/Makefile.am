xorgmodinputdir = $(libdir)/xorg/modules/input

xorgmodinput_LTLIBRARIES = ft5x_drv.la

ft5x_drv_la_LDFLAGS = -module -avoid-version
ft5x_drv_la_SOURCES = ft5x.c
ft5x_drv_la_CFLAGS = $(LIBXSERVER_CFLAGS)
ft5x_drv_la_LIBADD = $(LIBXSERVER_LIBS)

