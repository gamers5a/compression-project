SET(gtest_build_tests OFF)
ADD_SUBDIRECTORY(gtest-1_7_0)

TARGET_NAME()

ADD_LIBRARY("${TARGET_NAME}" STATIC gtest.h gtest.cpp)
TARGET_LINK_LIBRARIES("${TARGET_NAME}" gtest)
TARGET_INCLUDE_DIRECTORIES("${TARGET_NAME}" PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/gtest-1_7_0/include")

ADD_LIBRARY("${TARGET_NAME}_main" STATIC gtest.h gtest.cpp)
TARGET_LINK_LIBRARIES("${TARGET_NAME}_main" gtest_main)
TARGET_INCLUDE_DIRECTORIES("${TARGET_NAME}_main" PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/gtest-1_7_0/include")
