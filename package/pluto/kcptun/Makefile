#
# Copyright (C) 2015-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v3.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=k3kcptun
PKG_VERSION:=20180316
PKG_RELEASE:=0

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	TITLE:=kcptun_for_k3
	DEPENDS:=@TARGET_bcm53xx_DEVICE_phicomm-k3 @PACKAGE_luci-app-kcptun +luci-app-kcptun
	URL:=https://github.com/xtaci/kcptun/releases
endef

define Package/$(PKG_NAME)/description
  kcptun for k3
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef


define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_DATA) ./files/usr/bin/kcptun_client  $(1)/usr/bin/kcptun_client
endef
$(eval $(call BuildPackage,$(PKG_NAME)))
