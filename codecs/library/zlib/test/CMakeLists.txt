TARGET_NAME()

ADD_EXECUTABLE("${TARGET_NAME}" test.cpp)
TARGET_LINK_LIBRARIES("${TARGET_NAME}" library-tests_common library-zlib)

ADD_TEST(NAME "${TARGET_NAME}" COMMAND "${TARGET_NAME}" DEPENDS "${TARGET_NAME}")