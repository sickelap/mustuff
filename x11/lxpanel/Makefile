# $OpenBSD$

COMMENT =	The standard panel of LXDE
DISTNAME =	lxpanel-0.9.3

SHARED_LIBS +=  lxpanel                   0.0 # 0.0

CATEGORIES =	x11

HOMEPAGE =	https://lxde.org

MAINTAINER =	Genadijus Paleckis <rwx@openbsd.lt>

# LGPL
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =		${MASTER_SITE_SOURCEFORGE:=lxde/}
EXTRACT_SUFX =		.tar.xz

WANTLIB +=		X11

MODULES =		textproc/intltool
BUILD_DEPENDS =		x11/gtk+2 \
			x11/libfm/core \
			x11/keybinder \
			devel/libwnck

RUN_DEPENDS =		x11/gtk+2 \
			x11/libfm/core \
			x11/lxmenu-data

CONFIGURE_STYLE =	gnu
CONFIGURE_ARGS =	--with-plugins=cpu,cpufreq,batt

FAKE_FLAGS =		sysconfdir=${PREFIX}/share/examples/lxpanel

CFLAGS =		-I${X11BASE}/include
LDFLAGS =		-L${X11BASE}/lib

.include <bsd.port.mk>
