set(SOURCE_FILES
    "test.cpp"
)

find_package(Catch2 CONFIG REQUIRED)
add_executable(tests ${SOURCE_FILES})
target_link_libraries(tests PRIVATE Catch2::Catch2 Catch2::Catch2WithMain)

include(CTest)
include(Catch)
catch_discover_tests(tests)
