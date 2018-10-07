cmake_minimum_required(VERSION 2.8)
project(ceres-hello)
set (CMAKE_CXX_STANDARD 11)

# ceres
#find_package(Ceres REQUIRED PATHS "/home/controller/3rdParty_REPO_gcc5.4.0/ceres-solver-1.12.0/" )
find_package(Ceres REQUIRED)
include_directories(${CERES_INCLUDE_DIRS})


add_executable(${PROJECT_NAME} "main.cpp")
target_link_libraries(${PROJECT_NAME} ${CERES_LIBRARIES})


