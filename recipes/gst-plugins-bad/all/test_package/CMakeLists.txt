cmake_minimum_required(VERSION 3.15)
project(test_package)


include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

find_package(gst-plugins-bad CONFIG REQUIRED)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} gst-plugins-bad::gst-plugins-bad)
