# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# 项目信息
project (Demo3_1)

# 查找目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)

# 添加子目录
include_directories(./hello ./world)

# 制定添加其他源文件
# 必须是制定hello.cc，不能用通配符方式或者目录直接替代，否则参考Demo3_2
set(HELLO_SRC hello/hello.cc)
set(WORLD_SRC world/world.cc)

# 指定生成目标
add_executable(Demo ${DIR_SRCS} ${HELLO_SRC} ${WORLD_SRC})
