# CMakeLists.txt para SumatraNext

# Versión mínima de CMake requerida
cmake_minimum_required(VERSION 3.10)

# Definición del proyecto
project(SumatraNext VERSION 0.1.0 LANGUAGES C CXX)

# --- Inicio de la migración ---
# Este es el punto de partida para migrar la compilación de SumatraPDF
# desde la solución de Visual Studio a CMake.
#
# El objetivo es replicar todos los ejecutables y bibliotecas
# que se definen en vs2022/SumatraPDF.sln.
#
# Iremos añadiendo subdirectorios y definiendo los "targets"
# de forma incremental.

add_subdirectory(ext/zlib)
add_subdirectory(ext/libwebp)

# Por ahora, este archivo solo establece la base del proyecto.
