file(GLOB_RECURSE headers "${CMAKE_CURRENT_LIST_DIR}/include/cyclone/*.h")
# file(GLOB_RECURSE headers "${CMAKE_CURRENT_LIST_DIR}/src/*.cpp" "${CMAKE_CURRENT_LIST_DIR}/src/caffe/opencv-caffe.proto" "${CMAKE_CURRENT_LIST_DIR}/src/onnx/opencv-onnx.proto")
file(GLOB_RECURSE src "${CMAKE_CURRENT_LIST_DIR}/src/*.cpp")

set(include_dirs "${CMAKE_CURRENT_LIST_DIR}/include/")

# set(SOURCE_FILES ${CMAKE_CURRENT_SOURCE_DIR}/src)


add_library(cyclone STATIC ${src} ${headers})
set_target_properties(cyclone PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(cyclone PRIVATE ${include_dirs})
# message(${CMAKE_CURRENT_SOURCE_DIR})