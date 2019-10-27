# Setup-for-deep-learning
Software setup guide for deep learning. The first step to setup your own deep learning environment is to check the version that the frameworks or tools support. If you're going to install `tensorflow-gpu`, you can check the version of CUDA and cuDNN that TensorFlow supports at https://www.tensorflow.org/install/gpu#software_requirements, or if you're going to install `pytorch`, you can refer to https://pytorch.org/get-started/locally/ or https://pytorch.org/get-started/previous-versions/.

According to the official websites, CUDA 10.0 is compatilble with `tensorflow-gpu=2.0` and `pytorch=1.1`.

Next, CUDA 10.0

# Ubuntu 16.04 + Nvidia Driver 410.78 + CUDA 10.0 + cuDNN 7.6.0 + Anaconda3
## Nvidia Driver 410.78


## CUDA 10.0
You can download `deb` file at https://developer.nvidia.com/cuda-toolkit-archive. For installer type, please, choose `deb (local)`, and then you can download the `deb` file.

Move to the directory that has the `deb` file, and type the command below.
```
sudo dpkg -i cuda-repo-ubuntu1604-10-0-local-10.0.130-410.48_1.0-1_amd64.deb
```
Next, we should add `apt-key` and the terminal tells you what command you should type to add the key.
After adding the key, type the commands below to install CUDA 10.0
```
sudo apt-get update
sudo apt-get install cuda-10-0
```

After installing it, you should set the path for CUDA.
```
sudo vim ~/.bashrc
```
And then, append the two lines at the bottom of `.bashrc`.
```
export PATH=/usr/local/cuda-10.0/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-10.0/lib64:$LD_LIBRARY_PATH
```
Finally, type the command below to apply the update.
```
source ~/.bashrc
```

## cuDNN 7.6.0

## Anaconda3
