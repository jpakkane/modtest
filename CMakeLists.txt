cmake_minimum_required(VERSION 3.24...3.28)
project(modtest CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(modtest
)

target_sources(modtest
  PUBLIC
  PRIVATE
    main.cpp
  PRIVATE
  FILE_SET CXX_MODULES
  BASE_DIRS  "${CMAKE_CURRENT_SOURCE_DIR}"
  FILES
    src0.ixx
    src1.ixx
    src2.ixx
    src3.ixx
    src4.ixx
    src5.ixx
    src6.ixx
    src7.ixx
    src8.ixx
    src9.ixx
)

target_compile_features(modtest PUBLIC cxx_std_20)
