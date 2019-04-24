cmake_minimum_required(VERSION 3.0.0)

project(WebAssembly-CMake-CrossCompileDemo)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${opencv_test_SOURCE_DIR}/bin)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_BUILD_TYPE Release)

find_package(OpenCV REQUIRED)

include_directories("${PROJECT_SOURCE_DIR}/include")
set(EXECUTABLE_OUTPUT_PATH "${PROJECT_SOURCE_DIR}/www")
set(LIBRARY_OUTPUT_PATH "${PROJECT_SOURCE_DIR}/lib")

aux_source_directory("${PROJECT_SOURCE_DIR}/src" SOURCE_LIST)
add_executable(hello "${PROJECT_SOURCE_DIR}/src/hello.cc")
add_executable(export1 "${PROJECT_SOURCE_DIR}/src/export1.cc")

add_executable(opencv_test "${PROJECT_SOURCE_DIR}/src/opencvtest.cpp")
link_directories(${OpenCV_LIBRARY_DIRS})
target_link_libraries(opencv_test ${OpenCV_LIBS})