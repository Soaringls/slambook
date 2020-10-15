# cmake_minimum_required(VERSION 2.8)
# project(slambook)

# set(CMAKE_CXX_FLAGS "-std=c++11 -03")
# # set(CMAKE_CXX_FLAGS "-std=c++14 -O3")
# set(CMAKE_BUILD_TYPE Debug)

# set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/bin)
# set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

# #deps pcl
# find_package(PCL 1.8 REQUIRED)
# add_definitions(${PCL_DEFINITIONS})

# find_package(Threads)
# find_package(OpenCV 4 REQUIRED)
# find_package(Sophus REQUIRED)
# find_package(Pangolin REQUIRED)
# #deps optimizal
# list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
# find_package(Ceres REQUIRED)
# find_package(G2O REQUIRED)

# #deps include
# include_directories(
#         ${PCL_LIBRARY_DIRS}    #pcl
#         ${OpenCV_INCLUDE_DIRS} #opencv
#         ${G2O_INCLUDE_DIRS} ${CERES_INCLUDE_DIRS}  #optimizal
#         # ${Sophus_INCLUDE_DIRS}
#         "/usr/local/include/sophus"
#         # "/usr/include/eigen3"
#         "/usr/include/eigen3.3.7"
#         ${Pangolin_INCLUDE_DIRS}
# )
# #deps deps-libs
# link_directories(${PCL_LIBRARY_DIRS})
# set(THIRD_LIBS 
#    ${OpenCV_LIBS}
#    ${Pangolin_LIBRARIES}
#    #optimizal
#    ${CERES_LIBRARIES} ${G2O_CORE_LIBRARY} ${G2O_STUFF_LIBRARY} #g2o_core g2o_stuff
# )

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/version2/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/version2/lib)

add_subdirectory(src)