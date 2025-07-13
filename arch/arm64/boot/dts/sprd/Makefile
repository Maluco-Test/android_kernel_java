# SPDX-License-Identifier: GPL-2.0

ifeq ($(BSP_BUILD_DT_OVERLAY),y)

ifeq ($(BSP_BUILD_ANDROID_OS),y)

ifeq ($(BSP_BUILD_FAMILY),sharkl5Pro)
dtbo-$(CONFIG_ARCH_SPRD) += \
	ums512-1h10-overlay.dtbo \
	p352-overlay.dtbo \
        ums512-1h10_go-overlay.dtbo \
        p353-overlay.dtbo \
	ums512-2h10-overlay.dtbo

ums512-1h10-overlay.dtbo-base := ums512.dtb
p352-overlay.dtbo-base := ums512.dtb
ums512-1h10_go-overlay.dtbo-base := ums512.dtb
p353-overlay.dtbo-base := ums512.dtb

ums512-2h10-overlay.dtbo-base := ums512.dtb

endif #//BSP_BUILD_ANDROID_OS

else #//AiAiAi or No DTBO
dtb-$(CONFIG_ARCH_SPRD) += \
	ums512-w27v1.dtb \
	ums512.dtb
dtbo-$(CONFIG_ARCH_SPRD) += \
	ums512-1h10-overlay.dtbo \
	p352-overlay.dtbo \
	ums512-1h10_go-overlay.dtbo \
	p353-overlay.dtbo

endif #//BSP_BUILD_DT_OVERLAY

always		:= $(dtb-y) $(dtbo-y)
subdir-y	:= $(dts-dirs)
clean-files	:= *.dtb *.dtbo

endif #//BSP_BUILD_DT_OVERLAY
