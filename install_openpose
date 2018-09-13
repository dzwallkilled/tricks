The installation is done using cmake.

Prerequisities:
    1. CUDA 8, cuDNN 5.1
        (if not installed, go to the openpose dir after git clone. The Openpose provides the installation shell script.)
        sudo ubuntu/install_cuda.sh
        sudo ubuntu/install_cudnn.sh
    2. Caffe
        e.g. ~/caffe/
    3. OpenCV (dependencies)
    4. There might be some other prerequisties for Caffe installation. 

Prerequisties installation:
1. sudo apt-get update
2. apt-get install libopencv-dev

Caffe Installation (if not installed): (e.g. installation dir: ~/caffe)
1. cd ~
2. git clone https://github.com/CMU-Perceptual-Computing-Lab/caffe.git
3. cd caffe
4. mkdir build
5. cd build
6. cmake ..
7. make all -j8
8. make test -j8
9. make runtest -j8
10. make install 

Openpose Installation: (e.g., installation dir: ~/openpose)
1. cd ~
2. git clone https://github.com/CMU-Perceptual-Computing-Lab/openpose
3. cd openpose
4. mkdir build
5. cd build
6. cmake -DCaffe_INCLUDE_DIRS=/home/"${USER}"/caffe/build/install/include \
  -DCaffe_LIBS=/home/"${USER}"/caffe/build/install/lib/libcaffe.so -DBUILD_CAFFE=OFF ..
7. make -j8
8. sudo make install

More details of installation refer to: https://github.com/CMU-Perceptual-Computing-Lab/openpose/blob/master/doc/installation.md

Usage:
cd ~/openpose
./build/examples/openpose/openpose.bin --video examples/media/video.avi --write_video output/result.avi --write_keypoint_json output/

More details of usage refer to: https://github.com/CMU-Perceptual-Computing-Lab/openpose/blob/master/doc/demo_overview.md

