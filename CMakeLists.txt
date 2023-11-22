cmake_minimum_required(VERSION 3.16)
project(upo_nhoa_msgs)

find_package(catkin REQUIRED COMPONENTS
	std_msgs
	sensor_msgs
	geometry_msgs

	message_generation
)

add_message_files(FILES
	BoundingBox2D.msg
	Detection2D.msg
	DetectionList2D.msg
)

#add_service_files(FILES
#	(Service files go here)
#)

#add_action_files(DIRECTORY action FILES
#	(Action files go here)
#)

generate_messages(DEPENDENCIES
	std_msgs
	sensor_msgs
	geometry_msgs
)

catkin_package(
	CATKIN_DEPENDS
		std_msgs
		sensor_msgs
		geometry_msgs

		message_runtime
)
