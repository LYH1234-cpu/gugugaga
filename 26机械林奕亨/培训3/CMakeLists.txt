cmake_minimum_required(VERSION 3.10)
project(training3)

find_package(OpenCV REQUIRED)

add_executable(task1_image task1_image.cpp)
target_link_libraries(task1_image ${OpenCV_LIBS})

add_executable(task2_video task2_video.cpp)
target_link_libraries(task2_video ${OpenCV_LIBS})
target_include_directories(task1_image PRIVATE ${OpenCV_INCLUDE_DIRS})
add_executable(task2_video task2_video.cpp)
target_link_libraries(task2_video ${OpenCV_LIBS})
target_include_directories(task2_video PRIVATE ${OpenCV_INCLUDE_DIRS})
