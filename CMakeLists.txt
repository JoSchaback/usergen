cmake_minimum_required(VERSION 3.10.0)

#project name
project (usergen)

add_executable(usergen usergen.c)

# Link the math library
target_link_libraries(usergen m)