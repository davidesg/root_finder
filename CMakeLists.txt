cmake_minimum_required(VERSION 3.10)
project(RootFinder
        VERSION 1.0
        DESCRIPTION "Herramienta para cálculo de raíces polinómicas"
        LANGUAGES C)

# Configuración estándar C (C99 para máxima compatibilidad)
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Configuración específica para cada compilador
if(CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    add_compile_options(-Wall -Wextra -pedantic -O2)
elseif(MSVC)
    add_compile_options(/W3 /O2)
endif()

# Fuente principal
add_executable(root root.c)

# Enlazar biblioteca matemática (solo en UNIX)
if(UNIX OR APPLE)
    target_link_libraries(root m)
endif()

# Instalación multiplataforma
install(TARGETS root
        RUNTIME DESTINATION bin
        BUNDLE DESTINATION bin)
