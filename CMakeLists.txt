cmake_minimum_required(VERSION 3.31)

project(cramer LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CPP_ROOT "src/cpp")

# Source files
set(INC_DIR src/cpp/include)
set(SRC_DIR src/cpp)
set(SRC_DIR src/cpp)
set(SOURCES ${SRC_DIR}/hello.cpp)

# Add executable target with source files listed in SOURCE_FILES variable
add_executable(${PROJECT_NAME} ${SOURCES})
target_precompile_headers(${PROJECT_NAME} PRIVATE ${INC_DIR}/pch.h)