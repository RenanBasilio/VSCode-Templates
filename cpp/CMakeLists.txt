# CMake build script for building an executable application.
#
# Building from source:
# > cmake . -Bbuild -DLIBDIR:STRING=<library directory>
# > cmake --build .

cmake_minimum_required(VERSION 3.9)
project(a 
        DESCRIPTION "Template project."
        VERSION 0.0.0)

enable_language(CXX)
set(CMAKE_CXX_STANDARD 11)

# Add header directory to project
include_directories(include)

# Add a submodule to the project
# include(libs/*/)

# Add an external library to the project
# find_package(LIB REQUIRED)
# include_directories(${LIB_INCLUDE_DIRS})

# Declare source files for build
set(
    SOURCE_FILES
    src/main.cpp
)

set(
    HEADER_FILES 
    include/main.hpp
)

# Set the name of the built executable
set(EXE_NAME "${PROJECT_NAME}-${PROJECT_VERSION}")

add_executable(${EXE_NAME} ${SOURCE_FILES})
set_target_properties(
    ${EXE_NAME} PROPERTIES
    VERSION 0
)

target_include_directories(${EXE_NAME} PUBLIC ${INCLUDE_DIRECTORIES})

# Link with an external package
# target_link_libraries(${EXE_NAME} ${LIB_LIBRARIES})

# Link with a submodule
# target_link_libraries(${EXE_NAME} ${SUBPROJECT_NAME})

# Copy dynamic libraries to executable directory if necessary
# add_custom_command(
#     TARGET ${PROJECT_NAME} POST_BUILD
#     COMMAND ${CMAKE_COMMAND} -E copy_if_different
#         ${LIB_SHARED_LIB}
#         $<TARGET_FILE_DIR:${PROJECT_NAME}>
# )