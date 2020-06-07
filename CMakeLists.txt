cmake_minimum_required(VERSION "3.0.0")
project("HelloWorld")

add_executable("${PROJECT_NAME}" "Main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION "${CMAKE_SOURCE_DIR}/Installed")
install(FILES "Main.cpp" DESTINATION "${CMAKE_SOURCE_DIR}/Installed")

INCLUDE(CTest)

add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")
#add_test("test2" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}" "someparam")