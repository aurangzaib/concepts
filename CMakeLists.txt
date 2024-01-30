cmake_minimum_required(VERSION 3.22.0)
project(concepts-cpp VERSION 0.1.0 LANGUAGES C CXX)

add_executable(concepts-cpp concepts-cpp/main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})

include(CPack)

find_package(xtensor REQUIRED)
target_include_directories(concepts-cpp PUBLIC ${xtensor_INCLUDE_DIRS})
target_link_libraries(concepts-cpp PUBLIC xtensor)