cmake_minimum_required(VERSION 3.10.0)
project(main VERSION 0.1.0 LANGUAGES C CXX)

add_executable(main log/main.cpp log/logger.cpp)
#实验
#add_executable(main log/main1.cpp )

target_include_directories(main PUBLIC include)


include(CTest)
enable_testing()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
