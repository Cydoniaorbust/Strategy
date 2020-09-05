cmake_minimum_required(VERSION 3.0)
project(Strategy)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
add_subdirectory(deps/CWGE)

set(SRC src/Source.cpp)
add_executable(Strategy ${SRC})

target_link_libraries(Strategy CWGE)

target_include_directories(Strategy PUBLIC deps/CWGE/include)
target_include_directories(Strategy PUBLIC include)