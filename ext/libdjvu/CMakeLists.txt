project(libdjvu CXX)

# Source files
file(GLOB_RECURSE LIBDJVU_SOURCES "*.cpp")

add_library(libdjvu STATIC ${LIBDJVU_SOURCES})

target_include_directories(libdjvu PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/../libjpeg-turbo
)

target_compile_definitions(libdjvu PUBLIC
    WIN32
    _WIN32
    WINVER=0x0605
    _WIN32_WINNT=0x0603
    _HAS_ITERATOR_DEBUGGING=0
    NDEBUG
    _CRT_SECURE_NO_WARNINGS
    NEED_JPEG_DECODER
    WINTHREADS=1
    DDJVUAPI=/**/
    MINILISPAPI=/**/
    DEBUGLVL=0
    _HAS_EXCEPTIONS=0
)

# Link against libjpeg-turbo
target_link_libraries(libdjvu PUBLIC jpeg-static)