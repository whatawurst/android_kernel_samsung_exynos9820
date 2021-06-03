# SPDX-License-Identifier: GPL-2.0
ifdef CONFIG_SOC_EXYNOS9820

  ifdef CONFIG_MACH_SAMSUNG_BEYOND0LTE

    dtb-y += exynos/exynos9820.dtb
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_24.dtbo
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_22.dtbo
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_19.dtbo
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_18.dtbo
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_17.dtbo
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_20.dtbo
    dtbo-y += samsung/exynos9820-beyond0lte_eur_open_25.dtbo

  endif
  ifdef CONFIG_MACH_SAMSUNG_BEYOND1LTE

    dtb-y += exynos/exynos9820.dtb
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_17.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_21.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_18.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_26.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_23.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_22.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_19.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_20.dtbo
    dtbo-y += samsung/exynos9820-beyond1lte_eur_open_24.dtbo

  endif
  ifdef CONFIG_MACH_SAMSUNG_BEYOND2LTE

    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_26.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_19.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_17.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_18.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_24.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_16.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_23.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_04.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_25.dtbo
    dtbo-y += samsung/exynos9820-beyond2lte_eur_open_20.dtbo
    dtb-y += exynos/exynos9820.dtb

  endif

  targets += dtbs
  DTB_LIST  := $(dtb-y) $(dtbo-y)
  always    := $(DTB_LIST)

  dtbs: $(addprefix $(obj)/, $(DTB_LIST))

  clean-files := *.dtb*

else
  dts-dirs += actions
  dts-dirs += al
  dts-dirs += allwinner
  dts-dirs += altera
  dts-dirs += amd
  dts-dirs += amlogic
  dts-dirs += apm
  dts-dirs += arm
  dts-dirs += broadcom
  dts-dirs += cavium
  dts-dirs += exynos
  dts-dirs += freescale
  dts-dirs += hisilicon
  dts-dirs += marvell
  dts-dirs += mediatek
  dts-dirs += nvidia
  dts-dirs += qcom
  dts-dirs += realtek
  dts-dirs += renesas
  dts-dirs += rockchip
  dts-dirs += socionext
  dts-dirs += sprd
  dts-dirs += xilinx
  dts-dirs += lg
  dts-dirs += zte

  subdir-y	:= $(dts-dirs)

  dtstree		:= $(srctree)/$(src)

  dtb-$(CONFIG_OF_ALL_DTBS) := $(patsubst $(dtstree)/%.dts,%.dtb, $(foreach d,$(dts-dirs), $(wildcard $(dtstree)/$(d)/*.dts)))

  always		:= $(dtb-y)

endif
