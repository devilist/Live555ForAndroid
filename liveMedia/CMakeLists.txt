# CMakeLists.txt in groupsock
# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_LIB_SRCS 变量
aux_source_directory(. DIR_LIB_SRCS)

##include引用其他目录下面的头文件
INCLUDE_DIRECTORIES(
        ${Live555ForAndroidIncludes}
)

#生成静态链接库
ADD_LIBRARY( liveMedia STATIC ${DIR_LIB_SRCS})
#链接其他静态库，如果不加此句，否则在link出现错误
TARGET_LINK_LIBRARIES(
        liveMedia
        BasicUsageEnvironment
        groupsock
        UsageEnvironment
        ws2_32
        winmm
)