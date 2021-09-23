#
# Copyright (C) 2016-2017 GitHub 
#
# This is free software, licensed under the GNU General Public License v3.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=xwcoco-passwall-settings
PKG_VERSION:=1.0
PKG_RELEASE:=1
PKG_LICENSE:=GPLv3
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=luci
  CATEGORY:=LuCI
  TITLE:=LuCI support for passwall Settings by xwcoco
  PKGARCH:=all
  DEPENDS:=+luci-base +luci-app-passwall
endef

define Package/$(PKG_NAME)/description
  Language Support for passwall Settings Packages.
endef


define Build/Configure
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/zzz-passwall-settings $(1)/etc/uci-defaults/99-xw-passwall-settings
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
