# cyton_gamma_hardware
Includes hardware drivers for the dynamixel motors 

Syntax for hardware: 
> roslaunch cyton_controllers controller_manager.launch

> roslaunch cyton_controllers start_controller.launch

> rosrun cyton_controllers dynamixel_joint_state_publisher.py

> roslaunch cyton_gamma_[1500 or 300]_moveit_config moveit_planning_execution.launch 2>/dev/null

> python command_front_end.py 2>/dev/null

OR Use this shell script, though currently not totally stable. In cyton_gamma_pkg/src.

> ./1500_hardware_launch.sh

# cyton_gamma_simulation
Syntax for Simulation: 
> roslaunch cyton_gamma_pkg simulation_gamma_[1500 or 300].launch 

This will start up the moveit client with RVIZ command center and simulation output in physics simulator (Gazebo was chosen for this application) 

These have been tested and allow cartesian, joint space, and force control. The gripper action controller is directly commanded since the internal dynamixel controllers do a fine job on a single axis joint. 

> standup.sh

This script will move the robot to a zero position. It's convenient for testing purposes and the same syntax can be used to command the robot directly with rostopic pub. 
