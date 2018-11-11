# $OpenBSD$

COMMENT =		control the lighting effects of Alienware computer

CATEGORIES =		sysutils

GH_ACCOUNT =		trackmastersteve
GH_PROJECT =		alienfx
GH_TAGNAME =		v2.3.4

# GPLv3+
PERMIT_PACKAGE_CDROM =	Yes

MODULES =		lang/python
MODPY_SETUPTOOLS =	Yes

RUN_DEPENDS =		devel/pyusb \
			devel/py-future

post-install:
	rm ${PREFIX}/bin/alienfx-gtk && \
	rm -rf ${PREFIX}/share/applications && \
	rm -rf ${PREFIX}/share/icons && \
	rm -rf ${PREFIX}/share/pixmaps && \
	rm -rf ${PREFIX}/share/man && \
	rm -rf ${PREFIX}lib/python${MODPY_VERSION}/site-packages/alienfx/ui && \
	rm -rf ${PREFIX}/lib/python${MODPY_VERSION}/site-packages/alienfx/data && \
	cp -R ${WRKSRC}/alienfx/data/themes ${PREFIX}/share/examples/alienfx


.include <bsd.port.mk>
