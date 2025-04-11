# Issues-Findings


# To select nvidia as the primary GPU : 

1. sudo apt install nvidia-prime

2. sudo prime-select nvidia
   


# TO fix git clone EOF error :
git config --global http.postBuffer 524288000


# To directly enter BIOS menu from UBUNTU without using the BIOS key :
sudo systemctl reboot --firmware-setup


# Source Gazebo Server :
source /usr/share/gazebo/setup.sh


# Torch with cuda for nvidia jetson platforms (with jetpack os):
https://forums.developer.nvidia.com/t/pytorch-for-jetson/72048

https://pytorch.org/TensorRT/getting_started/jetpack.html

pip install 'numpy<2'


# Ultralytics with torch and cuda compatiblity nvidia jetson series:
https://docs.ultralytics.com/guides/nvidia-jetson/
and then adjust numpy accordingly


# Gazebo server crashes randomly even for lightweight worlds.
Error message: [ERROR] [gzclient-2]: process has died [pid 4301, exit code -6, cmd 'gzclient'].


Solution: Add the following line to the .bashrc file : source /usr/share/gazebo/setup.sh

# Load Modbus on Jetson.

https://github.com/WCHSoftGroup/ch341ser_linux

cd ch341ser_linux/driver

make

sudo make install

to always load on boot: echo "ch341" | sudo tee -a /etc/modules

# SSH error (something Nasty).

ssh-keygen -f "/home/{user_name}/.ssh/known_hosts" -R "{IP}"

