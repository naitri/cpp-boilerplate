set(GTEST_SHUFFLE 1)

add_executable(
    cpp-test
    test.cpp
    ../app/pid.cpp
   
)

target_include_directories(cpp-test PUBLIC ../vendor/googletest/googletest/include 
                                           ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(cpp-test PUBLIC gtest)
