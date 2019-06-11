cmake_minimum_required(VERSION 3.14)
project(libclang_example)

set(CMAKE_CXX_STANDARD 11)
list(APPEND CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake_modules")

find_package(LibClang REQUIRED)

add_executable(libclang_example main.cpp)
target_include_directories(libclang_example PUBLIC ${LIBCLANG_INCLUDE_DIRS})
target_link_libraries(libclang_example ${LIBCLANG_LIBRARIES})
