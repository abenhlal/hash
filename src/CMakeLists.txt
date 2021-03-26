add_library(cborg-hash city.c fnv.c murmur.c)
target_link_libraries(cborg-hash PUBLIC cborg-hash-h)
install(TARGETS cborg-hash DESTINATION   ${CMAKE_INSTALL_LIBDIR}/cborg)