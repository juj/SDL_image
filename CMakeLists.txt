cmake_minimum_required(VERSION 2.8)

project(SDL_image)

#add_definitions(-Wall -Wcast-qual -Wextra -Wshadow -fno-exceptions -fno-rtti -pedantic -flto -m64)

file(GLOB_RECURSE sourceFiles IMG*.c)

include_directories(../SDL/include)

add_library(SDL_image STATIC ${sourceFiles})
