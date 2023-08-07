cmake_minimum_required(VERSION 3.0.2)
project(abb_irb5500_7axis_support)

find_package(catkin REQUIRED COMPONENTS
  rospy
)
catkin_package()

foreach(dir config launch meshes urdf)
   install(DIRECTORY ${dir}/
      DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach()
