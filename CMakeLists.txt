set(srcs
    "src/AccelStepper.cpp"
    "src/MultiStepper.cpp")

idf_component_register(SRCS "${srcs}"
                    INCLUDE_DIRS src
                    INCLUDE_DIRS include
                    REQUIRES driver
                    REQUIRES esp_timer
                    )


target_link_libraries(${COMPONENT_LIB} INTERFACE "-Wl,--undefined=uxTopUsedPriority")