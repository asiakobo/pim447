  zephyr_library()

  # Include the application include directory
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)

  zephyr_library_sources_ifdef(CONFIG_ZMK_PIMORONI_PIM447 src/pimoroni_pim447.c src/pimoroni_pim447_led.c)
