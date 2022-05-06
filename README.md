# REEF_estimator_sim_bundle

## Installation
```html
git clone https://github.com/uf-reef-avl/reef_estimator_sim_bundle
cd reef_estimator_sim_bundle
git submodule update --init --recursive
cd ../..
catkin_make
```

*Setting Up The Simulation**
-----------------------------

- To adjust the number of simulated vehicles modify the __launch_sim.launch__ file.  Changing the __spawn_turtles__ argument enables/disables the list of turtlebots.

- To switch between the two basic modes of flying (basic waypoints and Dubins path) change the __waypointmode__ argument.  Default behavior is __True__ which starts the basic waypoints algorithm.


**Running The Simulation**
--------------------------

- In one terminal run __python Master.py__ from the scripts directory.

- Wait a few seconds until __Autopilot ARMED__ and __RC override active__ are printed and then in another terminal run __roslaunch sim_estimator.launch__ from the launch directory.

- If the simulation is set to run the setpoint generator code, wait until __Takeoff!__ is printed in the second terminal and then use __rosparam set /setpoint_publisher/active true__ if you are using the setpoint_generator to start the simulated quadcopter.  Use __rosparam set /setpoint_publisher/active false__ to signal the quadcopter to head back to the origin.
Otherwise, if you are using dubins path, use __rosparam set /setpoint_publisher/activaction false__ to launch it.


