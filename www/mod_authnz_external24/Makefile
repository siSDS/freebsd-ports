# Created by: Jos� Garc�a Juanino <jjuanino@gmail.com>
# $FreeBSD$

PORTNAME=	mod_authnz_external
PORTVERSION=	3.3.2
CATEGORIES=	www
MASTER_SITES=	GOOGLE_CODE
PKGNAMESUFFIX=	24
DIST_SUBDIR=	apache24

MAINTAINER=	eugene@zhegan.in
COMMENT=	Allows users authentication based on external mechanisms on apache 2.4

LICENSE=	APACHE20

BROKEN=		Unfetchable (google code has gone away)

USE_APACHE=	24
AP_FAST_BUILD=	yes
AP_GENPLIST=	yes
SHORTMODNAME=	authnz_external
PROJECTHOST=	mod-auth-external

PORTDOCS=	AUTHENTICATORS INSTALL README	\
		CHANGES UPGRADE INSTALL.HARDCODE

post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	@${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
