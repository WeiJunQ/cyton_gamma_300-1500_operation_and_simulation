# cyton_gamma_simulation
simulation for cyton gamma 1500 with moveit motion planning

Includes hardware drivers for the dynamixel motors 

Syntax for hardware: 
> roslaunch cyton_controllers controller_manager.launch

> roslaunch cyton_controllers start_controller.launch

> catkin_ws/src/standup.sh

> rosrun cyton_controllers dynamixel_joint_state_publisher.py

> roslaunch cyton_gamma_1500_moveit_config moveit_planning_execution.launch



Syntax for Simulation: 
> roslaunch cyton_gamma_pkg simulation_gamma_1500.launch 

This will start up the moveit client with RVIZ command center and simulation output in physics simulator (Gazebo was chosen for this application) 

Note: The collision boundaries are pretty much destroyed. I haven't had time to fixing them yet, if the end effector's angle is angled downwards to close to the ground, robot may jump. Consider rviz to visualize these issues. 
