[![Build Status](https://drone.koma.link/api/badges/koma/check_zombie/status.svg)](https://drone.koma.link/koma/check_zombie)
# check_zombies for Nagios
This is a simple script to check the presence of zombies processes on the machine.

This script tries to take in consideration the fact hat sometime a Zombie pid is in this state for a short time because of the load or other environment events.
So it is possible to parametrize the tolleration.

``` 
Usage: [ -w <integer> ] [ -c <integer> ] [ -s <integer> ] [ -p ] [ -t ]
-w              (Optional) Minimum number of Zombie process to trigger warning. Default: 5
-c              (Optional) Minimum number of Zombie process to trigger critical. Default: 10
-s              (Optional) Maximum age in seconds. Default: 900
-p              (Optional) Print Performances data. Default: false
-p              (Optional) Process flag to be counted (Default to 'z,Z,+z,+Z')
-h               Print this help
Warning for compatibility mode you can execute the command with [ ./check_zombies WARN CRIT AGE_IN_SECS ] .
```
