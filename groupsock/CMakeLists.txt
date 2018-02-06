# CMakeLists.txt in groupsock
#编译源文件
SET(GROUPSOCK_SRCS
        GroupEId.cpp
        Groupsock.cpp
        GroupsockHelper.cpp
        inet.c
        IOHandlers.cpp
        NetAddress.cpp
        NetInterface.cpp
        )
#编译头文件
SET(GROUPSOCK_HEADERS
        include/GroupEId.hh
        include/Groupsock.hh
        include/GroupsockHelper.hh
        include/groupsock_version.hh
        include/IOHandlers.hh
        include/NetAddress.hh
        include/NetInterface.hh
        include/TunnelEncaps.hh

        )

##include引用其他目录下面的头文件
INCLUDE_DIRECTORIES(
        ${Live555ForAndroidIncludes}
)

#生成静态库
ADD_LIBRARY( groupsock STATIC ${GROUPSOCK_HEADERS} ${GROUPSOCK_SRCS})
#链接其他静态库，如果不加此句，否则在link出现错误
TARGET_LINK_LIBRARIES(
        groupsock
        BasicUsageEnvironment
        liveMedia
        UsageEnvironment
        ws2_32
        winmm
)