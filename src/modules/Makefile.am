
AUTOMAKE_OPTIONS = foreign
MODULE_FLAGS =     -module -avoid-version
INCLUDES =         -I $(top_srcdir)

if WITH_ELAN
ELAN_MODULE = qcmd.la
endif

if WITH_LIBGENDERS
if WITH_SDR
GENDERS_MODULE = genders-g.la
else
GENDERS_MODULE = genders.la
endif
endif

if WITH_NODEATTR
if WITH_SDR
NODEATTR_MODULE = nodeattr-g.la
else 
NODEATTR_MODULE = nodeattr.la
endif
endif

if WITH_NODEUPDOWN
NODEUPDOWN_MODULE = nodeupdown.la
endif

if WITH_RMS
RMS_MODULE = rms.la
endif

if WITH_MACHINES
MACHINES_MODULE = machines.la
endif

if WITH_SDR
SDR_MODULE = sdr.la
endif

pkglib_LTLIBRARIES = \
	sshcmd.la \
	xrcmd.la \
	$(ELAN_MODULE) \
	$(GENDERS_MODULE) \
	$(NODEATTR_MODULE) \
	$(NODEUPDOWN_MODULE) \
	$(RMS_MODULE) \
	$(MACHINES_MODULE) \
	$(SDR_MODULE)
	

xrcmd_la_SOURCES =        xrcmd.c
xrcmd_la_LDFLAGS =        $(MODULE_FLAGS)
sshcmd_la_SOURCES =       sshcmd.c
sshcmd_la_LDFLAGS =       $(MODULE_FLAGS)
qcmd_la_SOURCES =         qcmd.c
qcmd_la_LDFLAGS =         $(MODULE_FLAGS) $(top_builddir)/libqsw.la

machines_la_SOURCES =     machines.c
machines_la_LDFLAGS =     $(MODULE_FLAGS)
genders_la_SOURCES =      genders.c
genders_la_LDFLAGS =      $(MODULE_FLAGS) $(GENDERS_LIBS)
genders_g_la_SOURCES =    genders.c
genders_g_la_CFLAGS =     -DGENDERS_G_ONLY
genders_g_la_LDFLAGS =    $(MODULE_FLAGS)
nodeattr_la_SOURCES =     nodeattr.c
nodeattr_la_LDFLAGS =     $(MODULE_FLAGS)
nodeattr_g_la_SOURCES =   nodeattr.c
nodeattr_g_la_CFLAGS =    -DGENDERS_G_ONLY
nodeattr_g_la_LDFLAGS =   $(MODULE_FLAGS)
nodeupdown_la_SOURCES =   nodeupdown.c
nodeupdown_la_LDFLAGS =   $(MODULE_FLAGS) $(NODEUPDOWN_LIBS)
rms_la_SOURCES =          rms.c
rms_la_LDFLAGS =          $(MODULE_FLAGS)
sdr_la_SOURCES =          sdr.c
sdr_la_LDFLAGS =          $(MODULE_FLAGS)