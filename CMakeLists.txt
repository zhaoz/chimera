cmake_minimum_required(VERSION 2.6)

project(CHIMERA)

LINK_LIBRARIES(pthread ssl)

include_directories(${CHIMERA_SOURCE_DIR}/include)
add_subdirectory(src)
add_subdirectory(test)

SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/out/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/out/lib)

ADD_DEFINITIONS(-fPIC)
