# Swift Tensorflow Sample Project

Basic Tensorflow Functionality using Swift within Jupyter Notebook

## Requirements
* 8GB GPU
* Linux Mint 18.04
* CUDA Version 10.0.130
* CUDNN 7.4.1.5-1+cuda10.0 
* Anaconda3-2018.12-Linux-x86_64.sh

## Manual Install

## Install Swift-Tensorflow
```
sudo apt-get install git cmake ninja-build clang python uuid-dev libicu-dev icu-devtools libbsd-dev libedit-dev libxml2-dev libsqlite3-dev swig libpython-dev libncurses5-dev pkg-config libblocksruntime-dev libcurl4-openssl-dev systemtap-sdt-dev tzdata rsync

mkdir swift-tensorflow
cd swift-tensorflow/
wget https://storage.googleapis.com/s4tf-kokoro-artifact-testing/versions/v0.2/rc3/swift-tensorflow-RELEASE-0.2-cuda10.0-cudnn7-ubuntu18.04.tar.gz
tar -xvf swift-tensorflow-RELEASE-0.2-cuda10.0-cudnn7-ubuntu18.04.tar.gz
```

## Test Swift-Tensorflow
```
cd swift-tensorflow/
export PATH=$(pwd)/usr/bin:"${PATH}"
swift
```

### Create Conda Environment
```
conda create -n swift-tensorflow python==3.6
conda activate swift-tensorflow
conda install jupyter numpy matplotlib
git clone https://github.com/google/swift-jupyter
cd swift-jupyter
python register.py --sys-prefix --swift-python-use-conda --use-conda-shared-libs \
  --swift-toolchain /home/oryx/swift-tensorflow/usr
```

### Run Jupyter Notebook
```
conda activate swift-tensorflow
jupyter notebook
```
