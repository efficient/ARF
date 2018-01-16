cmake_minimum_required (VERSION 2.6)
project (ARF)

message(STATUS "Configuring..." ${CMAKE_PROJECT_NAME})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g -Wno-sign-compare -O3 -pthread -std=c++0x")

add_definitions(-DNDEBUG)

enable_testing()

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include")

add_subdirectory(src)
add_subdirectory(test)
