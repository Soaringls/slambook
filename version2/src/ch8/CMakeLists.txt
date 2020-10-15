cmake_minimum_required(VERSION 2.8)
project(ch8)

add_definitions("-DENABLE_SSE")
set(CMAKE_CXX_FLAGS "-std=c++11 ${SSE_FLAGS} -g -O3 -march=native")

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build/bin/${PROJECT_NAME})
set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build/lib/${PROJECT_NAME})

# find_package(OpenCV 4 REQUIRED)
# find_package(Sophus REQUIRED)
# find_package(Pangolin REQUIRED)

# include_directories(
#         ${OpenCV_INCLUDE_DIRS}
#         ${G2O_INCLUDE_DIRS}
#         # ${Sophus_INCLUDE_DIRS}
#         "/usr/local/include/sophus"
#         "/home/lyu/dexter/bak_gitopen/deps_libs/eigen/eigen-3.3.7"
#         ${Pangolin_INCLUDE_DIRS}
# )

add_executable(optical_flow optical_flow.cpp)
target_link_libraries(optical_flow ${THIRD_LIBS})

add_executable(direct_method direct_method.cpp)
target_link_libraries(direct_method ${THIRD_LIBS} )
