# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# 项目信息
project (Demo3_1)

# 查找目录下的所有源文件
# 并将名称保存到对应变量
aux_source_directory(. DIR_SRCS)
aux_source_directory(hello HELLO_SRC)
aux_source_directory(world WORLD_SRC)

# 添加子目录
include_directories(./hello ./world)

# 指定生成目标
add_executable(Demo ${DIR_SRCS} ${HELLO_SRC} ${WORLD_SRC})

