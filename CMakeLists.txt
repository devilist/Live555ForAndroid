#当前cmake版本号
cmake_minimum_required(VERSION 3.9)
#当前工程名称
project(Live555ForAndroid)

set(CMAKE_CXX_STANDARD 11)

#设置C++编译参数
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++11")

#设置可执行文件输出路径
SET(EXECUTABLE_OUTPUT_PATH ${Live555ForAndroid_SOURCE_DIR}/bin)
#设置链接lib输出路径
SET(LIBRARY_OUTPUT_PATH ${Live555ForAndroid_SOURCE_DIR}/lib)
#设置运行时查找输出路径
SET(RUNTIME_OUTPUT_DIRECTORY ${Live555ForAndroid_SOURCE_DIR}/bin)

#指定lib输出路径
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${Live555ForAndroid_SOURCE_DIR}/lib)
#指定bin为library输出路径
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${Live555ForAndroid_SOURCE_DIR}/bin)
#指定bin为Runtime输出路径
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${Live555ForAndroid_SOURCE_DIR}/bin)

#指定include头文件路径
SET(Live555ForAndroidIncludes
        ${Live555ForAndroid_SOURCE_DIR}/BasicUsageEnvironment/include
        ${Live555ForAndroid_SOURCE_DIR}/groupsock/include
        ${Live555ForAndroid_SOURCE_DIR}/liveMedia/include
        ${Live555ForAndroid_SOURCE_DIR}/UsageEnvironment/include
        )

#当前当前工程目录下面子目录
ADD_SUBDIRECTORY(BasicUsageEnvironment)
ADD_SUBDIRECTORY(groupsock)
ADD_SUBDIRECTORY(liveMedia)
ADD_SUBDIRECTORY(mediaServer)
ADD_SUBDIRECTORY(proxyServer)
ADD_SUBDIRECTORY(UsageEnvironment)
