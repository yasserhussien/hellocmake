cmake_minimum_required(VERSION "3.22.1")
project("HELLOWORLD")
add_executable("${PROJECT_NAME}" "main.cpp")
install(TARGETS "${PROJECT_NAME}" DESTINATION bin) #$(CMAKE_INSTALL_PREFIX)/bin
install(FILES "main.cpp" DESTINATION src) #$(CMAKE_INSTALL_PREFIX)/src
include(cTest)
add_test("test1" "${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")

