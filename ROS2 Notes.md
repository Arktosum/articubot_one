JOYSTICK MAPPING
		AXES:
		0 : LA LEFT (+1) / LA RIGHT (-1)
		1 : LA UP(+1) / LA DOWN (-1)
		2 : LT DEFAULT (+1) / ON PUSH (-1)
		3 : RA LEFT (+1) / RA RIGHT (-1)
		4 : RA UP(+1) / RA DOWN (-1)
		5 : RT DEFAULT (+1) / ON PUSH (-1)
		6 : ARROW LEFT (+1) / ARROW RIGHT (-1)
		7 : ARROW UP(+1) / ARROW DOWN (-1)
		
		BUTTONS

		0  : A
		1  : B
		2  : X
		3  : Y
		4  : LB
		5  : RB
		6  : BACK
		7  : START
		8  : HOME
		9 : LA PUSH
		10 : RA PUSH
		

// SET UP WORKSPACE

source install/setup.bash
colcon build --symlink-install

// LAPTOP SIM

ros2 launch articubot_one launch_sim.launch.py

ros2 launch articubot_one online_async_launch.py
ros2 launch articubot_one navigation_launch.py



// RASPBERRY PI

ros2 launch ldlidar_sl_ros2 ld14.launch.py
