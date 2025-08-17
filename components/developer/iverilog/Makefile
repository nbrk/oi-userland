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

BUILD_STYLE=		configure
USE_PARALLEL_BUILD=	yes

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		iverilog
COMPONENT_VERSION=	12.0
COMPONENT_SUMMARY=	Free compiler and simulator for the IEEE-1364 Verilog hardware description language
COMPONENT_FMRI=		developer/iverilog

COMPONENT_PROJECT_URL=	https://steveicarus.github.io/iverilog/
COMPONENT_SRC=          $(COMPONENT_NAME)-12_0
COMPONENT_ARCHIVE=      iverilog_v12_0.tar.gz
COMPONENT_ARCHIVE_URL=	https://github.com/steveicarus/iverilog/archive/refs/tags/v12_0.tar.gz
COMPONENT_ARCHIVE_HASH= sha256:a68cb1ef7c017ef090ebedb2bc3e39ef90ecc70a3400afb4aa94303bc3beaa7d
COMPONENT_LICENSE_FILE=	COPYING
COMPONENT_LICENSE=	GPLv2
COMPONENT_CLASSIFICATION= Development/Suites

COMPONENT_PRE_CONFIGURE_ACTION = \
        (cd $(SOURCE_DIR); aclocal; autoconf; $(CLONEY) $(SOURCE_DIR) $(@D))


include $(WS_MAKE_RULES)/common.mk

LDFLAGS+= -lsocket -licuuc

# Manually added build dependencies
REQUIRED_PACKAGES += developer/gperf

# Auto-generated dependencies
REQUIRED_PACKAGES += $(GCC_RUNTIME_PKG)
REQUIRED_PACKAGES += $(GXX_RUNTIME_PKG)
REQUIRED_PACKAGES += $(READLINE_PKG)
REQUIRED_PACKAGES += compress/bzip2
REQUIRED_PACKAGES += library/zlib
REQUIRED_PACKAGES += shell/ksh93
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/math
