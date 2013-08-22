CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

include(RezBuild)

FILE(GLOB_RECURSE py_files "python/*.py")

rez_install_python(python
	FILES ${py_files}
	RELATIVE
	DESTINATION .
)


rez_install_files(
	bin/hello_dummy
	DESTINATION .
	EXECUTABLE
)
