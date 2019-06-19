cmake_minimum_required(VERSION 3.8)
project(CPPExampleBot LANGUAGES CXX)

add_subdirectory(RLBotCPP)

add_executable(CPPExampleBot main.cc examplebot.cc examplebot.h)
target_link_libraries(CPPExampleBot RLBotCPP)
target_include_directories(CPPExampleBot PRIVATE RLBotCPP/inc RLBotCPP/lib/inc)
target_compile_features(CPPExampleBot PRIVATE cxx_std_17)