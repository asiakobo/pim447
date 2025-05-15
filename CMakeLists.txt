zephyr_library()

# Include the application include directory
zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
zephyr_include_directories(include)

zephyr_library_sources_ifdef(CONFIG_ZMK_PIM447 src/pimoroni_pim447.c src/pimoroni_pim447_led.c)
zephyr_library_sources_ifdef(CONFIG_ZMK_PIM447_BEHAVIORS src/behaviors/behavior_pim447.c)
