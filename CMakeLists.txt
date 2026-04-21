cmake_minimum_required(VERSION 3.10)
project(oj029_malloc_allocator C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS OFF)

add_executable(code
    vendor/malloclab-handout/mdriver.c
    vendor/malloclab-handout/memlib.c
    vendor/malloclab-handout/fsecs.c
    vendor/malloclab-handout/ftimer.c
    vendor/malloclab-handout/clock.c
    vendor/malloclab-handout/mm.c
)
target_include_directories(code PRIVATE vendor/malloclab-handout)
target_compile_options(code PRIVATE -O2 -pipe)
