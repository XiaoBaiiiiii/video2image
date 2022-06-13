cmake_minimum_required(VERSION 3.1)
project(video2image)

set(CMAKE_CXX_STANDARD 17)

project(video2image)
add_executable(video2image video2image.cc)

find_package(OpenCV REQUIRED)
find_package(Boost REQUIRED COMPONENTS system filesystem)

include_directories(${OpenCV_INCLUDE_DIRS} ${Boost_INCLUDE_DIRS})

# link_directories(video2image ${Boost_LIBRARY_DIRS})
target_link_libraries(video2image ${OpenCV_LIBRARIES} ${Boost_LIBRARIES})
