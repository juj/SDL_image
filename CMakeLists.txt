cmake_minimum_required(VERSION 2.8)

project(SDL_image)

#add_definitions(-Wall -Wcast-qual -Wextra -Wshadow -fno-exceptions -fno-rtti -pedantic -flto -m64)

# -DLOAD_JPG is also an option
add_definitions(-DLOAD_PNG -DLOAD_BMP -DLOAD_GIF -DLOAD_LBM -DLOAD_PCX -DLOAD_PNM -DLOAD_TGA -DLOAD_XCF -DLOAD_XPM -DLOAD_XV)

file(GLOB_RECURSE sourceFiles IMG*.c)

include_directories(../SDL/include)

add_library(SDL_image STATIC ${sourceFiles})

target_link_libraries(SDL_image png_static)
