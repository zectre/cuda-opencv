### Ubuntu-OpenCV
from https://github.com/jayrambhia/Install-OpenCV
if your system is Ubuntu, run the commands below.
```
$ cd Ubuntu
$ chmod +x * 
$ ./opencv_latest.sh
```


### CUDA
if your system is RedHat, run the commands below.
```
$ sudo dpkg -i cuda-repo-ubuntu1804-10-1-local-10.1.105-418.39_1.0-1_amd64.deb
$ sudo apt-key add /var/cuda-repo-<version>/7fa2af80.pub
$ sudo apt-get update
$ sudo apt install cuda-10.1
$ echo 'export PATH=/usr/local/cuda-10.1/bin:$PATH' >> ~/.bashrcInstall-OpenCV
```


### CUDNN
Download from https://developer.nvidia.com/rdp/cudnn-archive
```
$ tar -xzvf cudnn-10.1-linux-x64-v7.6.5.32.tgz
$ sudo cp -P cuda/include/cudnn.h /usr/local/cuda-10.1/include
$ sudo cp -P cuda/include/cudnn.h /usr/include/cudnn.h
$ sudo cp -P cuda/lib64/libcudnn* /usr/local/cuda-10.1/lib64/
$ sudo chmod a+r /usr/local/cuda-10.1/lib64/libcudnn*
```


### VERIFY
```
$ nvcc -V
$ cat /usr/local/cuda/version.txt
$ cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2
$ cat /usr/include/cudnn.h | grep CUDNN_MAJOR -A 2
```
