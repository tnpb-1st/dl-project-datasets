cmake_minimum_required(VERSION 3.27)
project(diabetic_ret_data)

# Find OpenCV package
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

# Find libzip package
find_package(libzip REQUIRED)
include_directories(${LIBZIP_INCLUDE_DIRS})

# Set source files
set(CMAKE_CXX_STANDARD 20)
set(SOURCES main.cpp)

# Add executable target
add_executable(diabetic_ret_data
        main.cpp)

# Link libraries
target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS} ${LIBZIP_LIBRARIES})
