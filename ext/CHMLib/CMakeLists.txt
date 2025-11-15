# CMakeLists.txt for the CHMLib library

# Define the chm static library
add_library(chm STATIC
    chm_lib.c
    lzx.c
)

# Add the current directory to the include path
target_include_directories(chm PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

# Add preprocessor definitions
target_compile_definitions(chm PRIVATE
    WIN32
    _WIN32
    _CRT_SECURE_NO_WARNINGS
    _HAS_EXCEPTIONS=0
)

# For Release builds, add NDEBUG
target_compile_definitions(chm PRIVATE
    $<$<CONFIG:Release>:NDEBUG>
)
