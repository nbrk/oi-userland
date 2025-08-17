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
# Copyright 2025 Nikolay Burkov <nbrk@linklevel.net>
#

BUILD_STYLE=		cmake
USE_PARALLEL_BUILD=	yes

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		Cataclysm-DDA
COMPONENT_VERSION=	0.H-RELEASE
COMPONENT_PROJECT_URL=	https://cataclysmdda.org/
COMPONENT_FMRI=		games/cataclysm-dda
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	 sha256:9fbd80d13321321d6ed1f5a736ab874e06d335429f2a51a39eefd2fa51feae68
COMPONENT_ARCHIVE_URL=	https://github.com/CleverRaven/Cataclysm-DDA/archive/refs/tags/$(COMPONENT_VERSION).tar.gz
COMPONENT_LICENSE=	CC AS 3.0
COMPONENT_LICENSE_FILE=	LICENSE.txt
COMPONENT_SUMMARY=	Cataclysm: Dark Days Ahead is a turn-based survival game set in a post-apocalyptic world
COMPONENT_CLASSIFICATION="Applications/Games"

include $(WS_MAKE_RULES)/common.mk

LDFLAGS+= -lsocket -licuuc

CMAKE_OPTIONS+=-DCMAKE_POLICY_VERSION_MINIMUM=3.20
CMAKE_OPTIONS+=-DCMAKE_BUILD_TYPE=Release # builds all localization files
CMAKE_OPTIONS+=-DCURSES=OFF
CMAKE_OPTIONS+=-DTILES=ON
CMAKE_OPTIONS+=-DSOUND=ON
CMAKE_OPTIONS+=-DGETTEXT_MSGFMT_EXECUTABLE=/usr/gnu/bin/msgfmt # incompatible with non-GNU msgfmt
CMAKE_OPTIONS+=-DCMAKE_CXX_FLAGS=-w

#CONFIGURE_ENV+= XGETTEXT=/usr/gnu/bin/xgettext
#CONFIGURE_OPTIONS += --with-xgettext=/usr/bin/gxgettext

# Auto-generated dependencies
REQUIRED_PACKAGES += text/gnu-gettext
# REQUIRED_PACKAGES += $(GCC_RUNTIME_PKG)
# REQUIRED_PACKAGES += $(GXX_RUNTIME_PKG)
# REQUIRED_PACKAGES += $(ICU_LIBRARY_PKG)
# REQUIRED_PACKAGES += compress/xz
# REQUIRED_PACKAGES += developer/icu
# REQUIRED_PACKAGES += image/library/libpng16
# REQUIRED_PACKAGES += library/c++/harfbuzz
# REQUIRED_PACKAGES += library/lzo
# REQUIRED_PACKAGES += library/sdl2
# REQUIRED_PACKAGES += library/zlib
# REQUIRED_PACKAGES += system/library
# REQUIRED_PACKAGES += system/library/fontconfig
# REQUIRED_PACKAGES += system/library/freetype-2
# REQUIRED_PACKAGES += system/library/math
# REQUIRED_PACKAGES += web/curl
