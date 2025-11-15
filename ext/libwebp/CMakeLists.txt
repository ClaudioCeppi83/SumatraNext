# CMakeLists.txt for the libwebp library

# Define the libwebp static library
add_library(libwebp STATIC
    src/dec/alpha_dec.c
    src/dec/buffer_dec.c
    src/dec/frame_dec.c
    src/dec/idec_dec.c
    src/dec/io_dec.c
    src/dec/quant_dec.c
    src/dec/tree_dec.c
    src/dec/vp8_dec.c
    src/dec/vp8l_dec.c
    src/dec/webp_dec.c
    src/dsp/alpha_processing.c
    src/dsp/alpha_processing_neon.c
    src/dsp/alpha_processing_sse2.c
    src/dsp/alpha_processing_sse41.c
    src/dsp/cost.c
    src/dsp/cpu.c
    src/dsp/dec.c
    src/dsp/dec_clip_tables.c
    src/dsp/dec_neon.c
    src/dsp/dec_sse2.c
    src/dsp/dec_sse41.c
    src/dsp/filters.c
    src/dsp/filters_neon.c
    src/dsp/filters_sse2.c
    src/dsp/lossless.c
    src/dsp/lossless_neon.c
    src/dsp/lossless_sse2.c
    src/dsp/lossless_sse41.c
    src/dsp/rescaler.c
    src/dsp/rescaler_neon.c
    src/dsp/rescaler_sse2.c
    src/dsp/ssim.c
    src/dsp/ssim_sse2.c
    src/dsp/upsampling.c
    src/dsp/upsampling_neon.c
    src/dsp/upsampling_sse2.c
    src/dsp/upsampling_sse41.c
    src/dsp/yuv.c
    src/dsp/yuv_neon.c
    src/dsp/yuv_sse2.c
    src/dsp/yuv_sse41.c
    src/utils/bit_reader_utils.c
    src/utils/bit_writer_utils.c
    src/utils/color_cache_utils.c
    src/utils/filters_utils.c
    src/utils/huffman_encode_utils.c
    src/utils/huffman_utils.c
    src/utils/palette.c
    src/utils/quant_levels_dec_utils.c
    src/utils/quant_levels_utils.c
    src/utils/random_utils.c
    src/utils/rescaler_utils.c
    src/utils/thread_utils.c
    src/utils/utils.c
)

# Add the src directory to the include path
target_include_directories(libwebp PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/src
)

# Add preprocessor definitions
target_compile_definitions(libwebp PRIVATE
    WIN32
    _WIN32
    _HAS_EXCEPTIONS=0
)

# For Release builds, add NDEBUG
target_compile_definitions(libwebp PRIVATE
    $<$<CONFIG:Release>:NDEBUG>
)