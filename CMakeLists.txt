cmake_minimum_required(VERSION 3.13)
project(fost-deps)


add_subdirectory(boost)
add_subdirectory(boringssl)

target_compile_options(boringssl_gtest PUBLIC
        $<$<COMPILE_LANGUAGE:CXX>:-Wno-c++20-extensions>
        -Wno-pedantic
    )
