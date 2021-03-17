add_library(hash-h INTERFACE)
target_include_directories(hash-h INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
install(FILES hash.h DESTINATION  ${CMAKE_INSTALL_INCLUDEDIR}/cborg)
install(FILES hash/city.h hash/fnv.h hash/murmur.h DESTINATION  ${CMAKE_INSTALL_INCLUDEDIR}/cborg/hash)