add_library(hash city.c fnv.c murmur.c)
target_link_libraries(hash PUBLIC hash-h)
install(TARGETS hash DESTINATION   ${CMAKE_INSTALL_LIBDIR}/cborg)