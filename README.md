# CUDA-installation
Install CUDA toolkit 10.1 on Linux 20.04

By defoult, Linux 20.04 has gcc 9.3; however, installing Cuda 10.1 requires lower version of gcc. So first I install gcc-6 and create a symbolic link to it as follows:

1- Go to **/etc/apt/sources.list** and add this link in the end **deb http://dk.archive.ubuntu.com/ubuntu/ bionic main universe**.

2- open a terminal and type:

*sudo apt update*

*sudo apt install g++-6*

3- Create a symbolic link:

*cd /usr/bin*

*sudo rm gcc*

*sudo ln -s /usr/bin/gcc-6 /usr/bin/gcc*

4- Now, download cuda toolkit and follow the instructions to install it.

https://developer.nvidia.com/cuda-10.1-download-archive-base?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1810&target_type=runfilelocal

5- Finally, export the library by adding the addresses to the **.bashrc** file as follows:

*cd*

*sudo gedit .bashrc*

**export PATH=/usr/local/cuda-10.1/bin${PATH:+:${PATH}}**

**export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64\
                         {LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}**
