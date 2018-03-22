project(ProgressBar)

cmake_minimum_required(VERSION 2.8)

set(CURSES_NEED_NCURSES TRUE)
find_package(Curses)
include_directories(${CURSES_INCLUDE_DIRS})

message(STATUS ${CURSES_LIBRARIES})

include_directories(include)

add_subdirectory(lib)
add_subdirectory(test)
