# Cyton_gamma_simulation
simulation for cyton gamma 1500 with moveit motion planning

Includes hardware drivers for the dynamixel motors 

Syntax for hardware: 
> roslaunch cyton_controllers controller_manager.launch
> roslaunch cyton_controllers start_controller.launch
> catkin_ws/src/standup.sh
> rosrun cyton_controllers dynamixel_joint_state_publisher.py
> roslaunch cyton_gamma_1500_moveit_config moveit_planning_execution.launch


Syntax for Simulation: 

