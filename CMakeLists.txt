cmake_minimum_required(VERSION 3.12)

project("rarcrack")
set(CMAKE_C_COMPILER "gcc")

aux_source_directory(${PROJECT_SOURCE_DIR} SRC_FILES)

add_executable(rarcrack ${SRC_FILES})

find_package(LibXml2 REQUIRED)
target_link_libraries(rarcrack PRIVATE LibXml2::LibXml2)