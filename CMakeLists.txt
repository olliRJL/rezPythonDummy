CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

include(RezBuild)

FILE(GLOB_RECURSE py_files "dummyModule/*.py")

rez_install_python(py
	FILES ${py_files}
	RELATIVE
	DESTINATION py
)


rez_install_files(
	bin/hello_dummy
	DESTINATION .
	EXECUTABLE
)
