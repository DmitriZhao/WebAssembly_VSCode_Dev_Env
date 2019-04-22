cmake_minimum_required(VERSION 3.0.0)

project(WebAssembly-CMake-CrossCompileDemo)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_BUILD_TYPE Release)

include_directories("${PROJECT_SOURCE_DIR}/include")
set(EXECUTABLE_OUTPUT_PATH "${PROJECT_SOURCE_DIR}/www")
set(LIBRARY_OUTPUT_PATH "${PROJECT_SOURCE_DIR}/lib")

aux_source_directory("${PROJECT_SOURCE_DIR}/src" SOURCE_LIST)
add_executable(demo "${SOURCE_LIST}")