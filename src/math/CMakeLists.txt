set(math_src
        src/math.cpp
        src/math.h)

add_library(shared SHARED ${math_src})
add_library(static STATIC ${math_src})