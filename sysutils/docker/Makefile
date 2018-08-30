# $OpenBSD$
#
ONLY_FOR_ARCHS=	amd64

COMMENT=	Docker CLI

DISTNAME=	v18.09.0-ce-tp4
PKGNAME=	docker-18.09.0-ce

HOMEPAGE=	https://www.docker.com/

MAINTAINER=	Genadijus Paleckis <rwx@openbsd.lt>

GH_ACCOUNT=	docker
GH_PROJECT=	cli
GH_TAGNAME=	${DISTNAME}

# Apache Licence 2.0
PERMIT_PACKAGE_CDROM=Yes

CATEGORIES=	sysutils

EXTRACT_SUFX=	.tar.gz

MODULES=	lang/go

TARGET=		github.com/docker/cli
ALL_TARGET=	${TARGET}/cmd/docker
WRKSRC=		${MODGO_WORKSPACE}/src/${TARGET}

do-install:
	${INSTALL_PROGRAM} ${MODGO_WORKSPACE}/bin/docker ${PREFIX}/bin/

.include <bsd.port.mk>
