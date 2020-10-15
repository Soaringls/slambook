cmake_minimum_required(VERSION 2.8)
project(ch6)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build/bin/${PROJECT_NAME})
set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build/lib/${PROJECT_NAME})

add_executable(gaussNewton gaussNewton.cpp)
target_link_libraries(gaussNewton ${THIRD_LIBS})#${OpenCV_LIBS})

add_executable(ceresCurveFitting ceresCurveFitting.cpp)
target_link_libraries(ceresCurveFitting ${THIRD_LIBS})#${OpenCV_LIBS} ${CERES_LIBRARIES})

# add_executable(g2oCurveFitting g2oCurveFitting.cpp)
# target_link_libraries(g2oCurveFitting ${THIRD_LIBS})#${OpenCV_LIBS} ${G2O_CORE_LIBRARY} ${G2O_STUFF_LIBRARY})
