cmake_minimum_required(VERSION 3.8)
project(robot_arm_urdf)

# 1. Use ament_cmake instead of catkin
find_package(ament_cmake REQUIRED)

# 2. Find dependencies individually (ROS 2 style)
find_package(urdf REQUIRED)
find_package(xacro REQUIRED)
find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)

# 3. Install your folders so 'ros2 launch' can find them
# This replaces the 'foreach' loop and CATKIN_PACKAGE_SHARE_DESTINATION
install(DIRECTORY
  config
  launch
  meshes
  urdf
  DESTINATION share/${PROJECT_NAME}
)

# 4. REQUIRED: This must be the very last line
ament_package()
