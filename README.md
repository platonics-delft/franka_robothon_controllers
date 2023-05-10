# Franka Cartesian Impedance Control for Robothon 2023 of Platonics Delft. 
To install:
- Create a workspace containing a src directory.
- Inside the src directory, clone the franka_ros repository by frankaemika.
- Inside the repository, clone this repository.
- Return to the workspace main directory (cd ../..).
- Source your version of ROS (e.g. ```source /opt/ros/melodic/setup.bash```).
- Build the project, calling: 
 ```
 catkin_make -DMAKE_BUILD_TYPE=Release -DFranka_DIR:PATH=/path/to/libfranka/build 
 ```

To run the controller:
- Switch on your Panda robot (make sure the gripper is initialized correctly), unlock its joints (and activate the FCI if necessary).
- Open a terminal, in every terminal: ```source devel/setup.bash```
- ```roslaunch franka_human_friendly_controllers cartesian_variable_impedance_controller.launch robot_ip:=ROBOT_IP load_gripper:=True```
