# Created by: Michael Johnson <ahze@FreeBSD.org>
# $FreeBSD$

PORTNAME=	mp4v2
PORTVERSION=	1.9.1
PORTREVISION=	1
CATEGORIES=	multimedia
MASTER_SITES=	GOOGLE_CODE

MAINTAINER=	multimedia@FreeBSD.org
COMMENT=	Library and tools to read, create, and modify mp4 files

BROKEN=		Unfetchable (google code has gone away)

CONFLICTS=	mpeg4ip-libmp4v2-[0-9.]*
USES=		compiler gmake libtool tar:bzip2
MAKEFILE=	GNUmakefile
GNU_CONFIGURE=	yes
USE_LDCONFIG=	yes
CONFIGURE_ENV=	"FOUND_HELP2MAN=no"

.include <bsd.port.pre.mk>

# GCC is broken with PCH: https://lists.freebsd.org/pipermail/svn-src-all/2015-March/101722.html
.if ${COMPILER_TYPE} == gcc
CONFIGURE_ARGS=	--disable-gch
.endif

.include <bsd.port.post.mk>
