# Information cmake
cmake_minimum_required(VERSION 3.0.2)

# set variables

set(CMAKE_SHARED_LIBRARY_PREFIX "")

# add subdirectory

# add executable and target libraries
add_library( launcher_client SHARED LauncherClient.cpp)

target_include_directories (launcher_client PRIVATE 
		../include/
		../
		../packages/
		../interfaces
		../submodules/lief/include
)

file(GLOB_RECURSE SOURCES
        *.cpp
)

target_sources(launcher_client PRIVATE 
		${SOURCES}
)