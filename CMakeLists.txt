cmake_minimum_required(VERSION 3.10)
project(MyGTK4Project)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK REQUIRED gtk4)

include_directories(${GTK_INCLUDE_DIRS})
link_directories(${GTK_LIBRARY_DIRS})
add_definitions(${GTK_CFLAGS_OTHER})

add_executable(example main.cpp)

target_link_libraries(example ${GTK_LIBRARIES})
