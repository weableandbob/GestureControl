cmake_minimum_required (VERSION 2.8)
project (GestureControl)
find_package (OpenCV REQUIRED)

if (UNIX)
    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -pedantic")
endif(UNIX)

add_executable (GestureControl GestureControl.cpp)
target_link_libraries (GestureControl ${OpenCV_LIBS})
