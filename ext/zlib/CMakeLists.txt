# CMakeLists.txt for the zlib library

# Define the zlib static library
add_library(zlib STATIC
    adler32.c
    compress.c
    crc32.c
    deflate.c
    gzclose.c
    gzlib.c
    gzread.c
    gzwrite.c
    inffast.c
    inflate.c
    inftrees.c
    trees.c
    zutil.c
)

# Add the current directory to the include path, so that zlib.h and zconf.h can be found
# by both zlib's own sources and by other libraries that link against zlib.
target_include_directories(zlib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

# Add preprocessor definitions that were in the .vcxproj file
target_compile_definitions(zlib PRIVATE
    WIN32
    _WIN32
    _HAS_EXCEPTIONS=0
)

# For Release builds, add NDEBUG
target_compile_definitions(zlib PRIVATE
    $<$<CONFIG:Release>:NDEBUG>
)