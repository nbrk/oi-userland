#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2016 Josef 'Jeff' Sipek <jeffpc@josefsipek.net>
# Copyright 2016 Jim Klimov <jimklimov@gmail.com>
# Copyright 2018 Harry Liebel <hliebel@gmail.com>
# Copyright 2025 Nikolay Burkov <nbrk@linklevel.net>
#

BUILD_STYLE=		cmake
USE_PARALLEL_BUILD=	yes

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		OpenTTD
COMPONENT_VERSION=	14.1
COMPONENT_PROJECT_URL=	http://www.openttd.org/en/
COMPONENT_FMRI=		games/openttd
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).zip
COMPONENT_ARCHIVE_HASH=	\
	sha256:8cde825809f168ce8b98f84d3d9b88bd1d769f3ab011e2b0fa8e613629666a79
COMPONENT_ARCHIVE_URL=	https://github.com/OpenTTD/OpenTTD/archive/refs/tags/$(COMPONENT_VERSION).zip
COMPONENT_LICENSE=	GPLv2
COMPONENT_LICENSE_FILE=	COPYING.md
COMPONENT_SUMMARY=	OpenTTD is an open source simulation game based upon Transport Tycoon Deluxe
COMPONENT_CLASSIFICATION="Applications/Games"

include $(WS_MAKE_RULES)/common.mk

LDFLAGS+= -lsocket -licuuc

# Auto-generated dependencies
REQUIRED_PACKAGES += $(GCC_RUNTIME_PKG)
REQUIRED_PACKAGES += $(GXX_RUNTIME_PKG)
REQUIRED_PACKAGES += $(ICU_LIBRARY_PKG)
REQUIRED_PACKAGES += compress/xz
REQUIRED_PACKAGES += developer/icu
REQUIRED_PACKAGES += image/library/libpng16
REQUIRED_PACKAGES += library/c++/harfbuzz
REQUIRED_PACKAGES += library/lzo
REQUIRED_PACKAGES += library/sdl2
REQUIRED_PACKAGES += library/zlib
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/fontconfig
REQUIRED_PACKAGES += system/library/freetype-2
REQUIRED_PACKAGES += system/library/math
REQUIRED_PACKAGES += web/curl
