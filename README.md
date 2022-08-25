# Installation-ROS-2-Humble-Hawksbill
Installing ROS 2 Humble Hawksbill desktop on Ubuntu 22.04 LTS

The Robot Operating System (ROS) is an open-source framework that helps researchers and developers build and reuse code between robotics applications. ROS is also a global open-source community of engineers, developers and hobbyists who contribute to making robots better, more accessible and available to everyone

## Installing 
In Ubuntu oprating open the and strt to Install the follwing 

### Set locale
```
locale
```
```
sudo apt update && sudo apt install locales
```
```
sudo locale-gen en_US en_US.UTF-8
```
```
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
```
```
export LANG=en_US.UTF-8
```
```
locale
```


### Setup Sources
You will need to add the ROS 2 apt repository to your system. First, make sure that the Ubuntu Universe repository is enabled by checking the output of this command
```
apt-cache policy | grep universe
```

This should output a line like the one below:
```
500 http://us.archive.ubuntu.com/ubuntu jammy/universe amd64 Packages
    release v=22.04,o=Ubuntu,a=jammy,n=jammy,l=Ubuntu,c=universe,b=amd64
```

If you don’t see an output line like the one above, then enable the Universe repository with these instructions.
```
sudo apt install software-properties-common
```
```
sudo add-apt-repository universe
```

Now add the ROS 2 apt repository to your system. First authorize our GPG key with apt
```
sudo apt update && sudo apt install curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```

Then add the repository to your sources list
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```







### Setup Sources
```
sudo apt update && sudo apt install locales
```
```
sudo locale-gen en_US en_US.UTF-8
```
```
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
```
```
export LANG=en_US.UTF-8
```
```
locale
```
