#
# Copyright (C) 2016-2017 GitHub 
#
# This is free software, licensed under the GNU General Public License v3.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=xwcoco-mosdns-settings
PKG_VERSION:=1.1
PKG_RELEASE:=49
PKG_LICENSE:=GPLv3
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=luci
  CATEGORY:=LuCI
  TITLE:=LuCI support for mosdns Settings by xwcoco
  PKGARCH:=all
  DEPENDS:=+luci-base +@LUCI_LANG_zh-cn
endef

define Package/$(PKG_NAME)/description
  Language Support Packages.
endef


define Build/Configure
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/mosdns
	$(INSTALL_BIN) ./files/config.yaml $(1)/etc/mosdns/config.yaml
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/zzz-mosdns-settings $(1)/etc/uci-defaults/99-mosdns-settings
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
