cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

add_subdirectory(binaryninja-api)

ADD_LIBRARY( libkbinja STATIC
        code.cpp )

target_link_libraries(libkbinja binaryninjaapi)

target_compile_features(libkbinja PRIVATE cxx_std_17 c_std_99)