# ros2-tf2


Following tutorial for ros foxy - 
https://docs.ros.org/en/foxy/Tutorials/Intermediate/Tf2/Introduction-To-Tf2.html


## Steps 

start docker 

```bash
docker run -it -v <absolute_path_to_this_repo>/ros2_tf2_ws/src/:/ros2_tf2_ws/src/ --name ros2_tf2 ros:foxy
```

```bash
source /opt/ros/foxy/setup.bash
ros2 topic list
```

```bash
ros2 topic list
ros2 topic info <topicName>
ros2 topic echo <topicName>

ros2 node list
ros2 node info <nodeName>
```
