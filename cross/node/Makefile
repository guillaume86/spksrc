PKG_NAME = node
PKG_VERS = 0.8.22
PKG_EXT = tar.gz
PKG_DIST_NAME = node-v$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://nodejs.org/dist/v$(PKG_VERS)
PKG_DIR = node-v$(PKG_VERS)

HOMEPAGE = http://www.nodejs.org/
COMMENT  = Evented I/O for V8 javascript.
LICENSE  =

# Configure
CONFIGURE_ARGS = --without-snapshot --dest-cpu=arm --dest-os=linux

# Compile
COMPILE_TARGET = myCompile

# Install
INSTALL_TARGET = myInstall

include ../../mk/spksrc.cross-cc.mk

.PHONY: myCompile
myCompile:
	$(RUN) $(MAKE) LD=$(TC_PATH)$(TC_PREFIX)g++

.PHONY: myInstall
myInstall:
	$(RUN) $(MAKE) install DESTDIR=$(INSTALL_DIR)
