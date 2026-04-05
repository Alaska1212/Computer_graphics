cmake_minimum_required(VERSION 3.10)
project(Computer_graphics)

set(CMAKE_CXX_STANDARD 17)

add_subdirectory(external)

add_executable(${PROJECT_NAME} src/main.cpp)

find_package(OpenGL REQUIRED)

set(libs
        ${OPENGL_LIBRARY}
        glfw
        glad
        glm
)

target_link_libraries(${PROJECT_NAME} ${libs})
