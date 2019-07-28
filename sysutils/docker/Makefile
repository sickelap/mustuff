# $OpenBSD$

ONLY_FOR_ARCHS =	amd64

COMMENT =		command line tool for Docker

VERSION =		18.09.1
DISTNAME =		v${VERSION}
PKGNAME =		docker-${VERSION}
CATEGORIES =		sysutils
HOMEPAGE =		https://www.docker.com/

GH_ACCOUNT =		docker
GH_PROJECT =		cli
GH_TAGNAME =		${DISTNAME}

# Apache Licence 2.0
PERMIT_PACKAGE =	Yes

MODULES =		lang/go

TARGET =		github.com/docker/cli
ALL_TARGET =		${TARGET}/cmd/docker
WRKSRC =		${MODGO_WORKSPACE}/src/${TARGET}

do-install:
	${INSTALL_PROGRAM} ${MODGO_WORKSPACE}/bin/docker ${PREFIX}/bin/
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/docker/completion/
	cp -R ${MODGO_WORKSPACE}/src/${TARGET}/docs/reference \
	  ${PREFIX}/share/doc/docker
	cp -R ${WRKSRC}/contrib/completion/{bash,fish,zsh} \
	  ${PREFIX}/share/examples/docker/completion/

.include <bsd.port.mk>
