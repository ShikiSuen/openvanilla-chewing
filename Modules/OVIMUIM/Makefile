# Makefile for OVIMUIM
#
# Copyright (c) 2004-2008 The OpenVanilla Project (http://openvanilla.org)
# All rights reserved.
# 
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
# 
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
# 2. Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in the
#    documentation and/or other materials provided with the distribution.
# 3. Neither the name of OpenVanilla nor the names of its contributors
#    may be used to endorse or promote products derived from this software
#    without specific prior written permission.
# 
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
# AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
# IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
# ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE
# LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
# CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
# SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
# INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
# CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
# ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
# POSSIBILITY OF SUCH DAMAGE.

UIMOS?=$(shell uname)

ifneq ("$(UIMOS)", "Darwin")
    $(error This module does not compile under OS that is not Mac OS X)
endif

BUILDER=xcodebuild
CONFIG?=Release
DSTROOT?=/
CMDLINETOOLROOT?=/opt/local

PROJECT=OVIMUIM.xcodeproj

PRODUCTS=$(DSTROOT)/Library/OpenVanilla/0.7.2/Modules/OVIMUIM.bundle

all:
	xcodebuild -project $(PROJECT) -configuration $(CONFIG) build $(MAKEFLAGS)

install:
	xcodebuild -project $(PROJECT) -configuration $(CONFIG) install $(MAKEFLAGS)

clean:
	xcodebuild -project $(PROJECT) -configuration $(CONFIG) clean $(MAKEFLAGS)

uninstall:
	rm -rf $(PRODUCTS)
