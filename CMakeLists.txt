cmake_minimum_required(VERSION 3.14)
project(lda C)

set(CMAKE_C_STANDARD 11)
add_definitions(-Wno-unused-result)

include_directories(.)

link_libraries(m)
add_executable(lda
        cokus.c
        cokus.h
        lda-alpha.c
        lda-alpha.h
        lda-data.c
        lda-data.h
        lda-estimate.c
        lda-estimate.h
        lda-inference.c
        lda-inference.h
        lda-model.c
        lda-model.h
        lda.h
        utils.c
        utils.h)

install(TARGETS lda RUNTIME DESTINATION bin)