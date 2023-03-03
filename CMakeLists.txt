cmake_minimum_required(VERSION 3.10)
project(NecroBot VERSION 1.0)
add_subdirectory(src)
configure_file(NecroBotConfig.h.in NecroBotConfig.h)
add_executable(NecroBot src/necrobot.cpp)
target_include_directories(NecroBot PUBLIC
                            "${PROJECT_BINARY_DIR}"
                            "${PROJECT_SOURCE_DIR}/src"
                            )