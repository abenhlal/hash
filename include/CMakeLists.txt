add_library(hash-h INTERFACE)
target_include_directories(hash-h INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
install(FILES cborg/hash.h DESTINATION  ${CMAKE_INSTALL_INCLUDEDIR}/cborg)
install(FILES cborg/hash/city.h cborg/hash/fnv.h cborg/hash/murmur.h DESTINATION  ${CMAKE_INSTALL_INCLUDEDIR}/cborg/hash)