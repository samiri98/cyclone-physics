file(GLOB_RECURSE headers "${CMAKE_CURRENT_LIST_DIR}/../common/include/*/*.h" "${CMAKE_CURRENT_LIST_DIR}/../common/utils/*.h")
file(GLOB_RECURSE src "${CMAKE_CURRENT_LIST_DIR}/../common/utils/*.cpp" "${CMAKE_CURRENT_LIST_DIR}/src/*.cpp")
set(include_dirs "${CMAKE_CURRENT_LIST_DIR}/../common/include/glew/" "${CMAKE_CURRENT_LIST_DIR}/../common/include/glut/" "${CMAKE_CURRENT_LIST_DIR}/../common/include/" "${CMAKE_CURRENT_LIST_DIR}/../common/utils/")
set(lib_dirs "${CMAKE_CURRENT_LIST_DIR}/../common/lib/" "${CMAKE_CURRENT_LIST_DIR}/../common/lib/glew/Win32/" "${CMAKE_CURRENT_LIST_DIR}/../common/lib/glut/")


add_executable(ragdoll_demo ${src} ${headers})
set_target_properties(cyclone PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(ragdoll_demo PRIVATE ${include_dirs})
target_link_directories(ragdoll_demo PRIVATE ${lib_dirs})
target_link_libraries(ragdoll_demo glew32s.lib freeglut.lib cyclone.lib)