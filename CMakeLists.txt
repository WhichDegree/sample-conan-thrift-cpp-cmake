cmake_minimum_required(VERSION 2.8.12)
project(hello)
add_compile_options(-std=c++11)

# Using the "cmake" generator
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

add_executable(server src/hello_server.cpp src/gen-cpp/helloSvc.cpp)
add_executable(client src/hello_client.cpp src/gen-cpp/helloSvc.cpp)
target_link_libraries(server CONAN_PKG::thrift)
target_link_libraries(client CONAN_PKG::thrift)
