CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

include(RezBuild)

# install python files
FILE(GLOB_RECURSE py_files "python/*.py")

rez_install_python(python
	FILES ${py_files}
	RELATIVE
	DESTINATION .
)


# install executables
rez_install_files(
	bin/hello_dummy
	DESTINATION .
	EXECUTABLE
)
