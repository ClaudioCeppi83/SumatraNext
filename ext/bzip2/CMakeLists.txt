# CMakeLists.txt for the bzip2 library

# Define the bzip2 static library
add_library(bzip2 STATIC
    bzip_all.c
)

# Add the current directory to the include path
target_include_directories(bzip2 PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

# Add preprocessor definitions from unarrlib.vcxproj
target_compile_definitions(bzip2 PUBLIC
    HAVE_BZIP2
    BZ_NO_STDIO
)
