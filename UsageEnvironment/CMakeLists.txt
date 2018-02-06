# CMakeLists.txt in UsageEnvironment
#源文件
SET(USAGE_ENVIRONMENT_SRCS
        HashTable.cpp
        strDup.cpp
        UsageEnvironment.cpp
        )
#头文件
SET(USAGE_ENVIRONMENT_HEADERS
        include/Boolean.hh
        include/HashTable.hh
        include/strDup.hh
        include/UsageEnvironment.hh
        include/UsageEnvironment_version.hh
        )
#包含头文件
INCLUDE_DIRECTORIES(
        ${Live555ForAndroidIncludes}
)
#生成静态库
ADD_LIBRARY( UsageEnvironment STATIC ${USAGE_ENVIRONMENT_HEADERS} ${USAGE_ENVIRONMENT_SRCS})