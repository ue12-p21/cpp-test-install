cmake_minimum_required (VERSION 3.0)
project(cpp_check_install)


# Compiler options 
include(${PROJECT_SOURCE_DIR}/cmake/setup_compiler.cmake)


# Activate ctest 
include ( CTest )
enable_testing ()

find_package(Doxygen 1.8.13)

if( DOXYGEN_FOUND )
    message("Doxygen is installed --- ok")
else()
    ##message(FATAL_ERROR "Doxygen is not available")
endif(DOXYGEN_FOUND)

add_subdirectory(src)


