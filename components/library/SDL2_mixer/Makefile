#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL)". You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright (c) 2025 Nikolay Burkov <nbrk@linklevel.net>
#

DROP_STATIC_LIBRARIES= yes
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		SDL2_mixer
COMPONENT_VERSION=	2.8.1
COMPONENT_SUMMARY=	Simple DirectMedia Layer - simple multi-channel audio mixer
COMPONENT_PROJECT_URL=	https://libsdl.org/
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH= sha256:cb760211b056bfe44f4a1e180cc7cb201137e4d1572f2002cc1be728efd22660
COMPONENT_ARCHIVE_URL=  https://github.com/libsdl-org/SDL_mixer/releases/download/release-$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_FMRI=	library/audio/sdl2-mixer
COMPONENT_CLASSIFICATION=	System/Multimedia Libraries
COMPONENT_LICENSE=	zlib
COMPONENT_LICENSE_FILE=	LICENSE.txt

TEST_TARGET= $(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

PATH= $(PATH.gnu)

# Auto-generated dependencies
REQUIRED_PACKAGES += library/sdl2
REQUIRED_PACKAGES += system/library
