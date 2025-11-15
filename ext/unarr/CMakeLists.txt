# CMakeLists.txt for the unarrlib library

# Define the unarrlib static library
add_library(unarrlib STATIC
    _7z/_7z.c
    common/conv.c
    common/crc32.c
    common/custalloc.c
    common/stream.c
    common/unarr.c
    lzmasdk/CpuArch.c
    lzmasdk/Ppmd7.c
    lzmasdk/Ppmd7Dec.c
    lzmasdk/Ppmd8.c
    lzmasdk/Ppmd8Dec.c
    rar/filter-rar.c
    rar/huffman-rar.c
    rar/parse-rar.c
    rar/rar.c
    rar/rarvm.c
    rar/uncompress-rar.c
    tar/parse-tar.c
    tar/tar.c
    zip/inflate.c
    zip/parse-zip.c
    zip/uncompress-zip.c
    zip/zip.c
)

# Add include directories
target_include_directories(unarrlib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_SOURCE_DIR}/ext/zlib
    ${CMAKE_SOURCE_DIR}/ext/bzip2
    ${CMAKE_SOURCE_DIR}/ext/lzma/C
)

# Add preprocessor definitions
target_compile_definitions(unarrlib PUBLIC
    HAVE_ZLIB
    HAVE_BZIP2
    HAVE_7Z
    BZ_NO_STDIO
    _7ZIP_PPMD_SUPPPORT
)

# Link against dependencies
target_link_libraries(unarrlib PUBLIC
    zlib
    bzip2
    lzma
)
