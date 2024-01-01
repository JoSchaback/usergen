cmake_minimum_required(VERSION 3.10.0)

#project name
project (usergen)

include(CTest)

add_executable(usergen usergen.c)

# Link the math library
target_link_libraries(usergen m)

add_test(NAME generate_single_user_name COMMAND usergen)
add_test(NAME generate_five_user_names COMMAND usergen -c 5)