#[[
This source file is part of the DocC open source project

Copyright (c) 2024 Apple Inc. and the DocC project authors
Licensed under Apache License v2.0 with Runtime Library Exception

See https://swift.org/LICENSE.txt for license information
#]]

cmake_minimum_required(VERSION 3.24)

project(LMDB
  LANGUAGES C)

# Set the build artifact directories to ensure that the generated products are
# colocated and findable for wiring up into the test suites across repositories.
# This pattern is applied to all Swift and LLVM repositories.
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_subdirectory(Sources)
add_subdirectory(cmake/modules)
