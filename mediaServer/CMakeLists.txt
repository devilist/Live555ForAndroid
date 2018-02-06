# CMakeLists.txt mediaServer directory
#头文件
SET(MEDIA_SERVER_HDRS
        DynamicRTSPServer.hh
        )

#源文件
SET(MEDIA_SERVER_SRCS
        DynamicRTSPServer.cpp
        live555MediaServer.cpp
        )

#包含头文件目录
INCLUDE_DIRECTORIES(
        ${Live555ForAndroidIncludes}
)

#主程序入口，可执行程序入口
ADD_EXECUTABLE(mediaServer ${MEDIA_SERVER_HDRS} ${MEDIA_SERVER_SRCS})
#链接库文件
TARGET_LINK_LIBRARIES(
        mediaServer
        BasicUsageEnvironment
        groupsock
        liveMedia
        UsageEnvironment
        ws2_32
        winmm
)