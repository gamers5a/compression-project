CMAKE_MINIMUM_REQUIRED(VERSION 3.2)

PROJECT(codecs)

INCLUDE(${CMAKE_CURRENT_LIST_DIR}/cmake/common.cmake)
ENABLE_TESTING()
IF(UNIX)
    SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14 -g")
ELSE()
    MESSAGE("TODO")
ENDIF()

INCLUDE_DIRECTORIES("${CMAKE_CURRENT_LIST_DIR}")

ADD_SUBDIRECTORY(external)
ADD_SUBDIRECTORY(library)
ADD_SUBDIRECTORY(tools)