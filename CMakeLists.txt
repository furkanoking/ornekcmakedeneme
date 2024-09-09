# ilk basta cmkae minimum required bakacaksın
cmake_minimum_required( VERSION 3.16)
set(CMAKE_CXX_COMPILER /usr/bin/g++)   # veya /usr/bin/clang++
set(CMAKE_C_COMPILER /usr/bin/gcc)     # veya /usr/bin/clang


project(cmakeogrenmekicin)


set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_COMPILER /usr/bin/g++)   # veya /usr/bin/clang++

file(GLOB MY_SOURCES "${CMAKE_SOURCE_DIR}/main_dosyam/*.cpp")
set(sources ${MY_SOURCES})


include_directories(${CMAKE_SOURCE_DIR}/main_dosyam)

add_executable(furkan_add my_add/main.cpp ${sources})

add_library(my_add my_add/main.cpp)
target_include_directories(furkan_add PUBLIC ${CMAKE_SOURCE_DIR}/main_dosyam)

target_link_libraries(furkan_add my_add)

