# Это стандартное решение
cmake_minimum_required(VERSION 3.10)

project(MyProject CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include_directories(${PROJECT_SOURCE_DIR}/src/header)

# Используем GLOB_RECURSE для поиска всех .cpp файлов
file(GLOB_RECURSE SOURCES "src/*.cpp") # Собираем лишь src

add_executable(MyApp "src/main.cpp" ${SOURCES})
