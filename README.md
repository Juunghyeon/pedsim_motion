# Pedestrian Simulator

![image](https://github.com/Juunghyeon/images/assets/78840944/2e1569a4-f548-49ab-b1e7-dc04f7ad98be)

## Features

- Walking & Sit actor
- Walking actor
- Running actor

## References

- <https://github.com/srl-freiburg/pedsim_ros>
- <https://classic.gazebosim.org/tutorials?tut=actor&cat=build_robo>

## Installation

```bash
cd [workspace]/src
git clone https://github.com/Juunghyeon/pedsim_motion.git
cd pedsim_motion/build
cmake ..
make
export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:[workspace]/build
cd ../worlds
gazebo --verbose Cafe.world
```