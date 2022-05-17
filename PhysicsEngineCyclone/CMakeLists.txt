include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include/cyclone)
set(SOURCE_FILES ${CMAKE_CURRENT_SOURCE_DIR}/src)


add_library(cyclone STATIC ${SOURCE_FILES})
set_target_properties(cyclone PROPERTIES LINKER_LANGUAGE CXX)
# message(${CMAKE_CURRENT_SOURCE_DIR})