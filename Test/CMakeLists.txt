cmake_minimum_required(VERSION 3.15)

project(Test)

add_subdirectory(lib/googletest)

include_directories(lib/googletest/googletest/include)
set(SOURCE_FILES Stack<Int>Test.cpp main.cpp Stack<char>Test.cpp)
add_executable(Test ${SOURCE_FILES})
target_link_libraries(Test gtest)

include_directories(../StackLibrary)
target_link_libraries(Test StackLibrary)