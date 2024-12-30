# Minimum required version of CMake
cmake_minimum_required(VERSION 3.10)

# Project name
project(LithiumRunner)

# Specify the C standard
set(CMAKE_C_STANDARD 23)
set(CMAKE_C_STANDARD_REQUIRED True)

# Add the executable
add_executable(main src/main.c)

# Set the output directory for the executable
set_target_properties(main PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})

# Custom target for "lithium" execution
add_custom_target(
    lithium
    COMMAND ${CMAKE_COMMAND} -E echo "Run ./build/main with arguments directly."
    COMMENT "Lithium custom target is a helper to run ./lithium with your arguments."
    VERBATIM
)
