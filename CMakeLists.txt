cmake_minimum_required(VERSION 3.31)
project(cramer LANGUAGES CXX)


# Project settings
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Dependencies
find_package(spdlog REQUIRED)

# Source files
set(CPP_ROOT "src/cpp")
set(INC_DIR ${CPP_ROOT}/include)
set(SRC_DIR ${CPP_ROOT})
set(SOURCES ${SRC_DIR}/hello.cpp)

# Add executable target with source files listed in SOURCE_FILES variable
add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} PRIVATE spdlog::spdlog)
target_precompile_headers(${PROJECT_NAME} PRIVATE ${INC_DIR}/pch.h)
