project("subprocess")
cmake_minimum_required(VERSION 3.15)

# Unit test is enabled if this is the main project
if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_CURRENT_SOURCE_DIR})
  add_subdirectory(test)
endif()

add_library(libsubprocess INTERFACE)

target_include_directories(libsubprocess INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})