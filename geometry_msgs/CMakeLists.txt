cmake_minimum_required(VERSION 2.8.3)
project(geometry_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs)

add_message_files(
  DIRECTORY msg
  FILES
  Point.msg
  Point32.msg
  Pose.msg
  PoseStamped.msg
  PoseWithCovariance.msg
  PoseWithCovarianceStamped.msg
  Quaternion.msg
  Transform.msg
  TransformStamped.msg
  Twist.msg
  TwistWithCovariance.msg
  Vector3.msg)

generate_messages(DEPENDENCIES std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime std_msgs)
