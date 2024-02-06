#[[
This source file is part of the DocC open source project

Copyright (c) 2024 Apple Inc. and the DocC project authors
Licensed under Apache License v2.0 with Runtime Library Exception

See https://swift.org/LICENSE.txt for license information
#]]

add_library(CLMDB
  mdb.c
  midl.c)
target_include_directories(CLMDB PUBLIC
  include)

set_property(GLOBAL APPEND PROPERTY LMDB_EXPORTS CLMDB)
