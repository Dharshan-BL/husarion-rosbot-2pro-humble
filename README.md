# husarion-rosbot-2pro-humble

Creating your docker image:

1) cd to folder containing docker
2) docker build -t shirke_image .
3) Run the docker using:
   ```
   docker run -it --rm --name my_rosbot_container \
    --net=host \
    --privileged \
    -e ROS_DOMAIN_ID=10 \
    my_rosbot_image
   ```
4) ```docker commit <container_name> <new_image_name>```
5) ```mkdir husarion_ws/src -p```
6) ```cd husarion_ws/src``` 
7) ```git clone https://github.com/micro-ROS/micro-ROS-Agent.git```
8) ```sudo apt upgrade libfastcdr-dev```
9) ``` cd husarion_ws/src```
10) ```git clone https://github.com/eProsima/Fast-CDR.git```
11) ```cd ~/husarion_ws```
12) ```colcon build --symlink-install```
13) ```echo "source /root/husarion_ws/install/local_setup.bash" >> ~/.bashrc```
14) ```sudo apt upgrade ros-humble-fastcdr```
15) ```git clone https://github.com/husarion/rosbot_ros.git```



---- New attempt ---- 
```docker run -it --rm -v /dev:/dev -v /dev/shm:/dev/shm --privileged --net=host microros/micro-ros-agent:humble serial -D /dev/ttyS4  serial -b 576000```






