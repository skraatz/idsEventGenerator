cmake_minimum_required(VERSION 3.0)
project(genesids)

# Find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)
include_directories(/usr/local/include/)
link_directories(/usr/local/lib)

# Populate a CMake variable with the sources
set(genesids_SRCS
    idsEventGenerator.cpp
)

# Tell CMake to create the helloworld executable
add_executable(genesids ${genesids_SRCS})
set_property(TARGET genesids PROPERTY CXX_STANDARD 11)
target_link_libraries(genesids curl)

