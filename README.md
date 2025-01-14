# ros2-tf2


Following tutorial for ros foxy - 
https://docs.ros.org/en/foxy/Tutorials/Intermediate/Tf2/Introduction-To-Tf2.html


## Steps 

start docker 

When docker service is not running:
docker: error during connect: Head "http://%2F%2F.%2Fpipe%2FdockerDesktopLinuxEngine/_ping": open //./pipe/dockerDesktopLinuxEngine: The system cannot find the file specified. 

```bash
docker run -it -v <absolute_path_to_this_repo>/ros2_tf2_ws/src/:/ros2_tf2_ws/src/ --name ros2_tf2 ros:foxy
```

After the first time, to reconnect: (make sure to start the container is running first)
```bash
docker exec -it ros2_tf2 /bin/bash
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

Inside docker bash:


Static Broadcaster: https://docs.ros.org/en/foxy/Tutorials/Intermediate/Tf2/Writing-A-Tf2-Static-Broadcaster-Py.html

Basic Setup:

Along with the following make necessary changes to package.xml and CMakeLists.txt
```bash
root@b147ac78b837:/ros2_tf2_ws/src#ros2 pkg create --build-type ament_cmake learning_tf2


root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# mk
dir learning_tf2
root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# touch learning_tf2/__init__.py
root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# mk
dir scripts
root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# to
uch scripts/tf2_listener.py
root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# mkdir launch
root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# touch launch/learning_tf2_launch_1.py
root@b147ac78b837:/ros2_tf2_ws/src/learning_tf2# chmod +x scripts/tf2_listener.py 
```

All new Files in the scripts folder will need to be made into executables as well
