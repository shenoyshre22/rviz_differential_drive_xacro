cmake_minimum_required(VERSION 3.8)
project(xx_robot_description)

if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# Find core ROS 2 ament packages
find_package(ament_cmake REQUIRED)
find_package(urdf REQUIRED)

# Install the entire urdf folder containing your .urdf and .xacro files
install(DIRECTORY
  urdf
  DESTINATION share/${PROJECT_NAME}
)

# Install launch files if you create a launch directory later
if(EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/launch")
  install(DIRECTORY
    launch
    DESTINATION share/${PROJECT_NAME}
  )
endif()

ament_package()
