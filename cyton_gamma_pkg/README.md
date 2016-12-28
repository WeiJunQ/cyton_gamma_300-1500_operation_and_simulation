# cyton_gamma_pkg
This package contains the launch files used for simulation and execution on hardware for cyton series robots in ROS Indigo- and a commanding front-end for operations

## cyton_gamma_pkg/launch
Here are the launch files for each type of execution on the Cyton Gamm 1500 and Gamma 300. 

>simulation_gamma_[300 or 1500].launch

This will launch a simulation environment in RVIZ and Gazebo

>gamma_[1500 or 300]_planning_execution.launch

This is an edited version of the ROS-I generated file. It is tuned with removed parts not relavent for my implementation. Additional parameters were added for hardware execution. 

The remaining files, _gaz and _rviz support the simulation package. controllers.yaml in the index of the directory are for the simulation environment for Gazebo.

## cyton_gamma_pkg/src
Here are the python tests of a trajectory generation program, front-end, and path planning class utilizing OMPL and MoveIt.

> python command_front_end.py 

Will launch the front-end with accompanying OMPL/MoveIt planning backend class in robot_planning_class.py. 

test_traj.py shows how to fill out the trajectory_msgs JointTrajectory type in python and submit those commands directly to hardware. This allows you to bypass a planning node and is independent of OMPL, requiring only a connection to the hardware. 