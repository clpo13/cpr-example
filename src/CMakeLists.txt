add_executable(example example.cpp)
target_link_libraries(example PRIVATE cpr::cpr)
include_directories(${cpr_SOURCE_DIR}/include ${json_SOURCE_DIR}/include)
