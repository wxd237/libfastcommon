project(libfastcommon C)

cmake_minimum_required(VERSION 2.8)

if(CMAKE_C_COMPILER_ID MATCHES "GNU")
  set(CMAKE_C_FLAGS "-Wall")
  set(CMAKE_C_FLAGS_RELEASE "-g -O3")
  set(CMAKE_C_FLAGS_DEBUG "-g -DDEBUG_FLAG ")
endif()

add_definitions(-D_FILE_OFFSET_BITS=64 -D_GNU_SOURCE)

add_subdirectory(src)


