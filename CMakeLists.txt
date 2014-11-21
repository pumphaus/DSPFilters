cmake_minimum_required(VERSION 2.8)

# Enable C++11
if ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "Clang" OR "${CMAKE_CXX_COMPILER_ID}" STREQUAL "GNU")
    set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-std=c++0x")
elseif ("${CMAKE_CXX_COMPILER_ID}" STREQUAL "Intel")
    if (WIN32)
        set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "/Qstd=c++0x")
    else()
        set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-std=c++0x")
    endif()
else()
    message("Unknown compiler, assuming C++11 support doesn't require additional compiler flags")
endif()

add_subdirectory(src)
