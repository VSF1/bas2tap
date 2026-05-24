cmake_minimum_required(VERSION 3.10)
project(bas2tap VERSION 2.6 LANGUAGES C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

add_executable(bas2tap bas2tap.c)

# Apply compiler flags from the original makefile
target_compile_options(bas2tap PRIVATE -Wall -O2)

# Link the math library
target_link_libraries(bas2tap PRIVATE m)

install(TARGETS bas2tap DESTINATION bin)