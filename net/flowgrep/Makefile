# Created by: Corey Smith
# $FreeBSD$

PORTNAME=	flowgrep
PORTVERSION=	0.9
PORTREVISION=	1
CATEGORIES=	net security
MASTER_SITES=	http://www.monkey.org/~jose/software/flowgrep/
DISTNAME=	flowgrep-${PORTVERSION}

MAINTAINER=	corsmith@gmail.com
COMMENT=	TCP stream/UDP/IP payload 'grep' utility

RUN_DEPENDS=	${PYTHON_SITELIBDIR}/nidsmodule.so:net/pynids

LICENSE=	BSD4CLAUSE  # actually 3, but advertising clause is there

USES=		python shebangfix
SHEBANG_FILES=	flowgrep.py
NO_BUILD=	yes
NO_ARCH=	yes

PLIST_FILES=	sbin/flowgrep man/man8/flowgrep.8.gz

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/flowgrep.py \
		${STAGEDIR}${PREFIX}/sbin/flowgrep
	${INSTALL_MAN} ${WRKSRC}/flowgrep.8 ${STAGEDIR}${MANPREFIX}/man/man8

.include <bsd.port.mk>
