# roselito_agent

Executive functions for the ROSelito robot.

## Usage

To start the route recorder, call:
```bash
ros2 launch roselito_agent teach_route.launch save_path:=/absolute/path/to/route.pon
```

The `save_path` argument can be omitted, in which case the route is saved to a file named `route.pon` in the current folder.

To add the robot's current pose to the route, call:
```bash
ros2 launch roselito_agent push_waypoint.launch
```

To erase the last pose added to the route, call:
```bash
ros2 launch roselito_agent pop_waypoint.launch
```

To save the route file, call:
```bash
ros2 launch roselito_agent save_route.launch
```

To replay a recorded route, call:
```bash
ros2 launch roselito_agent replay_route.launch path:=/absolute/path/to/route.pon
```

The `path` argument can be omitted, in which case the route is loaded from a file named `route.pon` in the current folder.

When replaying routes in simulation, make sure to add the `use_sim_time` argument:
```bash
ros2 launch roselito_agent replay_route.launch path:=/absolute/path/to/route.pon use_sim_time:=true
```
