cmake_minimum_required(VERSION 3.11)
project(cpr-example)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FetchContent)

FetchContent_Declare(cpr
    GIT_REPOSITORY https://github.com/whoshuu/cpr.git)
FetchContent_GetProperties(cpr)
if(NOT cpr_POPULATED)
    FetchContent_Populate(cpr)
    add_subdirectory(${cpr_SOURCE_DIR} ${cpr_BINARY_DIR})
endif()

FetchContent_Declare(json
    GIT_REPOSITORY https://github.com/ArthurSonzogni/nlohmann_json_cmake_fetchcontent.git)
FetchContent_GetProperties(json)
if(NOT json_POPULATED)
    FetchContent_Populate(json)
    add_subdirectory(${json_SOURCE_DIR} ${json_BINARY_DIR} EXCLUDE_FROM_ALL)
endif()

add_executable(example example.cpp)
target_link_libraries(example PRIVATE cpr::cpr nlohmann_json::nlohmann_json)
include_directories(${cpr_SOURCE_DIR}/include ${json_SOURCE_DIR}/include)
