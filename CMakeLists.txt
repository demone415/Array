cmake_minimum_required(VERSION 2.8)

project(MyArray)

if (MSVC)
    add_definitions(/W4)
else()
    add_definitions(-Wall)
    add_definitions(-std=c++11)
endif()

include_directories(Catch/include)

include_directories(include)

enable_testing()

add_executable(test_array tests/test_array.cpp)

add_test(NAME ${PROJECT_NAME} COMMAND test_array)
