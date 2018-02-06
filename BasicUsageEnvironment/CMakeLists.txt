# CMakeLists.txt in BasicUsageEnvironment
##include引用其他目录下面的头文件
INCLUDE_DIRECTORIES(
        ${Live555ForAndroidIncludes}
)

# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_LIB_SRCS 变量
aux_source_directory(. DIR_LIB_SRCS)

#生成静态链接库,库为名BasicUsageEnvironment
ADD_LIBRARY(BasicUsageEnvironment STATIC ${DIR_LIB_SRCS})

