cmake_minimum_required(VERSION 2.8)

project(OpenGL_Exercises CXX)

SET( CMAKE_CXX_COMPILER /usr/bin/clang++ )

add_definitions( -std=c++14 -Wall )

include_directories( /usr/local/include )
link_directories( /usr/local/lib )

add_executable(window ${PROJECT_SOURCE_DIR}/src/main.cxx)

IF(APPLE)
  find_library( COCOA_LIBRARY Cocoa )
  find_library( OpenGL_LIBRARY OpenGL )
  find_library( IOKIT_LIBRARY IOKit )
  find_library( COREVIDEO_LIBRARY CoreVideo )
  SET( EXTRA_LIBS ${COCOA_LIBRARY} ${OpenGL_LIBRARY} ${IOKIT_LIBRARY} ${COREVIDEO_LIBRARY} )
ENDIF(APPLE)

target_link_libraries( window glfw3 ${EXTRA_LIBS} )
