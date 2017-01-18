cmake_minimum_required(VERSION 2.8.3)
project(omni3md CXX)

set(PDIR ${omni3md_SOURCE_DIR})
message(STATUS "Current directory: " ${PDIR})
find_package(Threads REQUIRED)
set(SDIR ${PDIR}/src)

set(MLIB_DIR ${PDIR}/libs)
link_directories(${MLIB_DIR})
include_directories(${omni3md_SOURCE_DIR}/include)

## Compile Omni3MD as a shared library
add_library(Omni3MD SHARED ${SDIR}/Omni3MD.cpp)
set_target_properties( Omni3MD
    PROPERTIES
    LIBRARY_OUTPUT_DIRECTORY ${MLIB_DIR}
)
target_compile_features(Omni3MD PRIVATE cxx_range_for)
##
