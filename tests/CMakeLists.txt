add_executable(test_city test_city.c)
add_test(test_city test_city)
target_link_libraries(test_city PUBLIC hash)

add_executable(test_fnv test_fnv.c)
add_test(test_fnv test_fnv)
target_link_libraries(test_fnv PUBLIC hash)

add_executable(test_murmur test_murmur.c)
add_test(test_murmur test_murmur)
target_link_libraries(test_murmur PUBLIC hash)