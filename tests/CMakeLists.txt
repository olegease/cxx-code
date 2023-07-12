# Ⓒ 2023 - Oleg'Ease'Kharchuk
link_libraries(c-corelib)
add_executable(test-c test.c)
add_test(c8hello test-c)

add_executable(test-cxx test.cxx)
add_test(cxx8hello test-cxx)
