# Bonus_task_husky

A husky terrain mapper using elevation mapping and octomap server.


## Deployment
- clone the workspace

```bash
  git clone 
```

- First build your workspace and add the source commands to your bash.

```bash
   catkin_make
```
```bash
   source devel/setup.bash
```
- launch the gazebo world with a terrain (I didnt use a mars terrain although it can be used as it still is in the husky_gazebo/world file change the file destination to terrain.launch)

```bash
   roslaunch husky_gazebo husky_playpen.launch
```
- to continue the octamapping , launch the octamapping node
```bash
   roslaunch octomap_server octomap_mapping.launch
```
- disselect occupied_cell_array or elevationmap    

    [octomap->(/occupied_cells_vis_array) , elevationmap->(/elevation_mapping/elevation_map)]
- launch the teleop node to control rover
``` bash
    rosrun husky_control keyboard.py
```
         

for more reference about robot launch the another rviz (not necessery might restart the elevation_mapping causing the rviz not accessable to the custom gridmap)
```bash
   roslaunch husky_viz view_robot.launch
   ```
- yt video link [here](https://youtu.be/gof3sf3Dt_k)
There are also several launch files like gmapping_demo , exploration_demo these launch the move_base launch file with global and local planners but here with out a static map it might be useless move the robot with the teleop to get a octomap or elevation_map more about both of them are here-

## Acknowledgements

 - [elevation mapping_used(ANYbotics)](https://github.com/ANYbotics/elevation_mapping)


- [octomap_used](https://github.com/OctoMap/octomap_mapping)
