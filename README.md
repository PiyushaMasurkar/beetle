This is beetle by TEAM MARUTI

#launch
ros2 launch beetle launch_sim.launch.py

#to publish joint_states
ros2 run joint_state_publisher joint_state_publisher

#to launch slam toolbox
ros2 launch slam_toolbox online_async_launch.py params_file:=./src/beetle/config/mapper_params_online_async.yaml use_sim_time:=true

#to save map 
ros2 run nav2_map_server map_saver_cli -f my_map

#to load rviz as it is
rviz2 -d src/beetle/config/main.rviz 