cmake_minimum_required(VERSION 3.5)
set(CMAKE_CXX_STANDARD 17)

project(
    VigenereCipherBreaker
    VERSION 1.0
    LANGUAGES CXX)

# Explicitly list the test source code and headers. The Catch header-only unit
# test framework is stored in with the test source.
set(CMakeVigenereCipherBreaker_SRC
    src/nGramScorer.cpp
    src/vigenereCipher.cpp
    src/vigenereCipherBreaker.cpp
)
set(CMakeVigenereCipherBreaker_HEADER
    src/nGramScorer.h
    src/vigenereCipher.h
)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

add_executable(vigenereCipherBreaker ${CMakeVigenereCipherBreaker_SRC} ${CMakeVigenereCipherBreaker_HEADER})

target_link_libraries(vigenereCipherBreaker PRIVATE Threads::Threads)