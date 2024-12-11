#[[
This source file is part of the DocC open source project

Copyright (c) 2024 Apple Inc. and the DocC project authors
Licensed under Apache License v2.0 with Runtime Library Exception

See https://swift.org/LICENSE.txt for license information
#]]

set(LMDB_EXPORTS_FILE
  ${CMAKE_CURRENT_BINARY_DIR}/LMDBExports.cmake)
configure_file(LMDBConfig.cmake.in
  ${CMAKE_CURRENT_BINARY_DIR}/LMDBConfig.cmake)

get_property(LMDB_EXPORTS GLOBAL PROPERTY LMDB_EXPORTS)
export(TARGETS ${LMDB_EXPORTS}
  NAMESPACE LMDB::
  FILE ${LMDB_EXPORTS_FILE}
  EXPORT_LINK_INTERFACE_LIBRARIES)
