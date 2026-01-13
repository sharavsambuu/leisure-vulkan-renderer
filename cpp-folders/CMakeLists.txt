cmake_minimum_required(VERSION 3.28)

project("leisure-vulkan-renderer")

set(CMAKE_CXX_STANDARD 20)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake/sdl2)
list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake/assimp)
list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake/glm)

FIND_PACKAGE(Threads COMPONENTS REQUIRED)

include(FetchContent)

message(STATUS "Fetching stb library...")
FetchContent_Declare(
    stb
    GIT_REPOSITORY https://github.com/nothings/stb.git
)
FetchContent_MakeAvailable(stb)


message(STATUS "Fetching Entt")
FetchContent_Declare(
    entt
    GIT_REPOSITORY https://github.com/skypjack/entt.git
    GIT_TAG        main
)
FetchContent_MakeAvailable(entt)


message(STATUS "Adding sub folders...")

add_subdirectory("src/shs-vulkan-renderer")
add_subdirectory("src/hello-world-vulkan")
