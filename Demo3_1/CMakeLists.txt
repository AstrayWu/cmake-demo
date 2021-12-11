# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# 项目信息
project (Demo3_1)
aux_source_directory(. DIR_SRCS)

# 添加 math 子目录

# add_subdirectory(hello)
# add_subdirectory(world)
include_directories(./hello ./world)

set(HELLO_SRC hello/hello.cc)
set(WORLD_SRC world/world.cc)

add_executable(Demo ${DIR_SRCS} ${HELLO_SRC} ${WORLD_SRC})

