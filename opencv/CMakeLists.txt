cmake_minimum_required(VERSION 3.5)
project(yolov5-v6.1-opencv-onnxrun)
set(CMAKE_CXX_STANDARD 11)

set(OpenCV_DIR "/Data2/zengsheng/opencv4/install/lib/cmake/opencv4")
find_package(OpenCV 4 REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})

file(GLOB My_Source_Files ./*.cpp)
add_executable(yolov5-opencv-cpp ${My_Source_Files})
target_link_libraries(yolov5-opencv-cpp ${OpenCV_LIBS})