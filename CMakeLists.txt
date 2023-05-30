cmake_minimum_required(VERSION 3.22)

project(mdpack LANGUAGES CXX VERSION 0.0.1)

find_package(fmt CONFIG REQUIRED)
# target_link_libraries(main PRIVATE fmt::fmt)

find_package(Catch2 CONFIG REQUIRED)
add_executable(tests "test/test.cpp")
target_link_libraries(tests PRIVATE Catch2::Catch2 Catch2::Catch2WithMain)

include(CTest)
include(Catch)
catch_discover_tests(tests)
