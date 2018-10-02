# $OpenBSD$

COMMENT =		package Python scripts into self-executables

MODPY_EGG_VERSION =	3.3.1
DISTNAME =		PyInstaller-${MODPY_EGG_VERSION}
PKGNAME =		py-installer-${MODPY_EGG_VERSION}
CATEGORIES =		sysutils

HOMEPAGE =		https://www.pyinstaller.org

# Python
PERMIT_PACKAGE_CDROM =	Yes

MODULES =		lang/python

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes

RUN_DEPENDS =		security/py-pefile

FLAVORS =		python3
FLAVOR ?=

.if !${FLAVOR:Mpython3}
RUN_DEPENDS +=		devel/py-dis3
.endif

pre-build:
	cd $(WRKSRC)/bootloader && ${MODPY_BIN} waf all

post-install:
	rm -rf $(PREFIX)/lib/python${MODPY_VERSION}/site-packages/PyInstaller/bootloader/{Darwin,Windows,Linux}*
	find $(PREFIX)/lib/python${MODPY_VERSION}/site-packages/PyInstaller -type f -name *.orig | xargs rm

.include <bsd.port.mk>
