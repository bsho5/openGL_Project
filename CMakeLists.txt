cmake_minimum_required(VERSION 3.1)

project(
  Besho
  VERSION 1.0
  LANGUAGES CXX C)

find_package(glfw3 REQUIRED)

add_library(glad glad.c)
add_subdirectory(lib/glm-master)
# == exe ==
add_executable(opengl main.cpp)
target_link_libraries(opengl PRIVATE glad)
target_link_libraries(opengl PRIVATE glfw)
target_link_libraries(opengl PRIVATE glm)