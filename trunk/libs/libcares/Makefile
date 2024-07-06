include $(ROOTDIR)/rules.mk

PKG_NAME:=c-ares
PKG_VERSION:=1.32.2

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/c-ares/c-ares/releases/download/v$(PKG_VERSION)
PKG_HASH:=072ff6b30b9682d965b87eb9b77851dc1cd8e6d8090f6821a56bd8fa89595061

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

$(eval $(call BuildPackage,c-ares))

romfs:
	$(INSTALL_DIR) $(ROMFSDIR)/lib
	$(CP) $(PKG_INSTALL_DIR)/lib/libcares.so* $(ROMFSDIR)/lib/
