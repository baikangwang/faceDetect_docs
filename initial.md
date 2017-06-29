# Initial

## Install opencv

clone the script from [baikangwang/install-opencv-in-ubuntu.sh](https://gist.github.com/baikangwang/959f67d2eb50ff04edeec9bfe44dafc7) and run the specific version

* install-opencv-2.4.13-in-ubuntu.sh
* install-opencv-3.2.0-in-ubuntu.sh

Take version 2.4.13 for example 

```bash
git clone https://gist.github.com/959f67d2eb50ff04edeec9bfe44dafc7.git
cd 959f67d2eb50ff04edeec9bfe44dafc7
chmod +x install-opencv-2.4.13-in-ubuntu.sh
./install-opencv-2.4.13-in-ubuntu.sh
```

## Check if installation works

```bash
$ python
>>> import cv2
```

* __ImportError: No module named cv2__
    ```bash
    sudo apt-get install python-opencv
    ```
* __ImportError: libopencv_reg.so.3.1: cannot enable executable stack as shared object requires: Invalid argument__
    ```bash
    sudo apt-get install execstack
    sudo /usr/sbin/execstack -c /usr/local/lib/libopencv_*
    ```
* __libdc1394 error: Failed to initialize libdc1394__
    ```bash
    sudo ln -s /dev/null /dev/raw1394
    ```

## Clone source code

```bash
git clone https://github.com/shantnu/FaceDetect.git
```