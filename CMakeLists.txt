cmake_minimum_required(VERSION 3.10)

project(OpenGLTutorial)

find_package(OpenGL REQUIRED)

add_subdirectory(deps/glfw)

add_executable(app src/main.cpp deps/glad/src/glad.c)


target_link_libraries(app
    PRIVATE
        OpenGL::GL
        glfw
)
target_include_directories(app
    PRIVATE
        deps/glad/include
)
