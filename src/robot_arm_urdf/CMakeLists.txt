cmake_minimum_required(VERSION 3.8)
project(robot_arm_urdf)

# ROS 2 uses ament_cmake
find_package(ament_cmake REQUIRED)

# Install directories (config, launch, meshes, urdf) to the share folder
# This replaces the 'foreach' loop and catkin-specific variables
install(DIRECTORY
  config
  launch
  meshes
  urdf
  DESTINATION share/${PROJECT_NAME}
)

# This replaces catkin_package() and MUST be at the end
ament_package()
