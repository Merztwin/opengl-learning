cmake_minimum_required(VERSION 3.0.0)
project(glEnginePro02 VERSION 0.2.3)

enable_testing()

find_package(glfw3 3.3 REQUIRED)

include_directories(external)
add_executable(glEnginePro02 glad.c main.cc)
target_link_libraries(glEnginePro02 GL dl glfw)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
