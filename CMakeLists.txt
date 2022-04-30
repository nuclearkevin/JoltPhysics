include(${CMAKE_SOURCE_DIR}/scripts/CMakeUtils.cmake)

file(GLOB_RECURSE SOURCE_FILES
    Jolt/*.cpp
    Jolt/*.h
)

set(INCLUDE_DIRS
    ${CMAKE_CURRENT_SOURCE_DIR}
)

add_library(jolt ${SOURCE_FILES})

target_include_directories(jolt PRIVATE ${INCLUDE_DIRS})

set_target_properties(jolt PROPERTIES FOLDER dependencies)

GroupSourcesByFolder(jolt)
