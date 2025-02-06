cmake_minimum_required(VERSION 3.31)
project(SdlGlHelloWorld)

set(CMAKE_C_STANDARD 11)

find_package(SDL2 REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)

include_directories(SdlGlHelloWorld ${SDL2_INCLUDE_DIRS} ${GLEW_INCLUDE_DIRS})
include_directories(headers)

add_executable(SdlGlHelloWorld src/main.c)

target_link_libraries(SdlGlHelloWorld PRIVATE ${SDL2_LIBRARIES} ${OPENGL_LIBRARIES} ${GLEW_LIBRARIES})
