# CMakeLists.txt for the lzma library

# Define the lzma static library
add_library(lzma STATIC
    7zBuf.c
    7zDec.c
    7zIn.c
    7zStream.c
    Bcj2.c
    Bra.c
    Bra86.c
    LzFind.c
    LzFindMt.c
    Lzma2Dec.c
    LzmaDec.c
    LzmaEnc.c
    Threads.c
)

# Add the current directory to the include path
target_include_directories(lzma PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

# Add preprocessor definitions from unarrlib.vcxproj
target_compile_definitions(lzma PUBLIC
    HAVE_7Z
    _7ZIP_PPMD_SUPPPORT
)
