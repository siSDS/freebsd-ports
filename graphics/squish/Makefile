# Created by: Reinier de Blois <rddeblois@gmail.com>
# $FreeBSD$

PORTNAME=	squish
PORTVERSION=	1.10
PORTREVISION=	2
CATEGORIES=	graphics
MASTER_SITES=	http://libsquish.googlecode.com/files/

MAINTAINER=	rddeblois@gmail.com
COMMENT=	Open source DXT compression library

LICENSE=	MIT

BROKEN=		Unfetchable (google code has gone away)

USES=		uidfix
MAKE_ENV=	INSTALL_DIR=${STAGEDIR}${PREFIX}
PLIST_FILES=	include/squish.h \
		lib/libsquish.a lib/libsquish.so.1 lib/libsquish.so
MAKEFILE=	${FILESDIR}/BSDmakefile
USE_LDCONFIG=	yes

OPTIONS_RADIO=	RG1
OPTIONS_RADIO_RG1=	ALTIVEC SSE
OPTIONS_DEFAULT_amd64=	SSE
ALTIVEC_DESC=	Use Altivec instructions
RG1_DESC=	Optimizations Selection

ALTIVEC_CXXFLAGS=	-DSQUISH_USE_ALTIVEC=1 -maltivec
SSE_CXXFLAGS=		-DSQUISH_USE_SSE=2 -msse2

.include <bsd.port.mk>
