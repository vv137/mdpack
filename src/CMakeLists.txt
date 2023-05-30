set(SOURCE_FILES
    "main.cpp"
)

find_package(fmt CONFIG REQUIRED)

add_executable(main ${SOURCE_FILES})
target_link_libraries(main PUBLIC fmt::fmt)
install(TARGETS main DESTINATION ${INSTALL_BIN_DIR})
