#
# Copyright (C) 2016-2017 GitHub 
#
# This is free software, licensed under the GNU General Public License v3.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=xwcoco-home-settings
PKG_VERSION:=1.2
PKG_RELEASE:=49
PKG_LICENSE:=GPLv3
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/xwcoco-home-settings
  SECTION:=luci
  CATEGORY:=LuCI
  TITLE:=LuCI support for Home Settings by xwcoco
  PKGARCH:=all
  DEPENDS:=+luci-base +@LUCI_LANG_zh-cn
endef

define Package/xwcoco-home-settings/description
	Language Support Packages.
endef

define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/xwcoco-home-settings/install
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/zzz-home-settings $(1)/etc/uci-defaults/99-home-settings
endef

$(eval $(call BuildPackage,xwcoco-home-settings))
