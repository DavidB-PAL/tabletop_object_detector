### Forked ROS Package: tabletop_object_detector

This is a fork of the ROS Fuerte release of tabletop_object_detector, <br>
from the pr2_object_manipulation stack: <br>
https://code.ros.org/svn/wg-ros-pkg/stacks/pr2_object_manipulation/branches/0.6-branch/perception/tabletop_object_detector/

The 0.6 branch has a few minor changes that are not shown in the old Trunk: <br>
https://code.ros.org/svn/wg-ros-pkg/stacks/pr2_object_manipulation/trunk/perception/tabletop_object_detector/

The ROS Wiki is incorrect, and the new Trunk (Groovy-devel) is at: <br>
https://github.com/ros-interactive-manipulation/pr2_object_manipulation/tree/groovy-devel/perception/tabletop_object_detector

These fixes & modifications are for using this node as part of the ROS Manipulation Pipeline, for robots other than the PR2. These changes have been tested to not break the simulated PR2 robot in ROS Fuerte Gazebo. <br>
-- David Butterworth, PAL Robotics S.L.
<br>

<br>
**Changelist:**

 - Fixed so each Rviz marker object has its own namespace e.g. graspable_object_0, graspable_object_1, etc. rather than all being in the same namespace, each time the node is run.

 - Fixed the handling of 'return_clusters' & 'return_models' parameters. Combined with the fix to tabletop_collision_map_processing, this means that if you don't request return_clusters, it will only return the table information; and if you don't request models, it should not attempt to do model fitting.

