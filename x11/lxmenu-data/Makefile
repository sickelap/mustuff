# $OpenBSD: Makefile.template,v 1.77 2018/02/09 17:08:33 sthen Exp $

COMMENT =	Application menu definitions files for LXDE
DISTNAME =	lxmenu-data-0.1.5

CATEGORIES =	x11

HOMEPAGE =	https://lxde.org

MAINTAINER =	Genadijus Paleckis <rwx@openbsd.lt>

# LGPL
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =		${MASTER_SITE_SOURCEFORGE:=lxde/}
EXTRACT_SUFX =		.tar.xz

RUN_DEPENDS =		x11/menu-cache

CONFIGURE_STYLE =	gnu
FAKE_FLAGS =		sysconfdir=${PREFIX}/share/examples/lxmenu-data

MODULES =		textproc/intltool

.include <bsd.port.mk>
