cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

project(pacman_opengl)

add_executable(pacman_opengl src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(pacman_opengl glfw)

add_subdirectory(external/glad)
target_link_libraries(pacman_opengl glad)
