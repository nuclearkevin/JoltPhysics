include(${CMAKE_SOURCE_DIR}/scripts/CMakeUtils.cmake)

file(GLOB_RECURSE SOURCE_FILES
    Jolt/*.cpp
    Jolt/*.h
)

add_library(jolt ${SOURCE_FILES})

target_include_directories(jolt PRIVATE Jolt)

set_target_properties(jolt PROPERTIES FOLDER dependencies)

GroupSourcesByFolder(jolt)
