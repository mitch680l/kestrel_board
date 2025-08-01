# Kconfig - nRF9151 Kestrel board configuration
#
# Copyright (c) 2024 Nordic Semiconductor
# SPDX-License-Identifier: LicenseRef-Nordic-5-Clause


if(CONFIG_BOARD_KESTREL_NRF9151_NS)
  # Use static partition layout to ensure the partition layout remains
  # unchanged after DFU. This needs to be made globally available
  # because it is used in other CMake files.
  set(PM_STATIC_YML_FILE ${CMAKE_CURRENT_LIST_DIR}/kestrel_nrf9151_pm_static.yml CACHE INTERNAL "")
endif()

# BMM350 minimal initialization removed - using AK09918C magnetometer instead
# The BMM350-specific power optimization is not applicable to AK09918C


