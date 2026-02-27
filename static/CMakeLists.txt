cmake_minimum_required(VERSION 3.13)

project(ufprog_static)

if(WIN32 OR MINGW OR BUILD_PORTABLE)
	set(EXAMPLE_DIR examples)
else()
	set(EXAMPLE_DIR ${DATA_DIR}/examples)
endif()

install(
	DIRECTORY ${ufprog_static_SOURCE_DIR}/examples/
	DESTINATION ${EXAMPLE_DIR}
)
