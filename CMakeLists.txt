
cmake_minimum_required( VERSION 3.19 )

project( widgets )

set( CMAKE_INCLUDE_CURRENT_DIR ON )
set( CMAKE_AUTOMOC ON )

option( BUILD_WIDGETS_EXAMPLES "Build examples" ON )

find_package( Qt6Core REQUIRED )
find_package( Qt6Gui REQUIRED )
find_package( Qt6Widgets REQUIRED )

set( CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/lib )

add_subdirectory( src )

if( BUILD_WIDGETS_EXAMPLES )
	add_subdirectory( examples )
endif()
