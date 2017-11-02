
# References

## Blog Post
* [TensorFlow meets PyTorch with Eager execution](https://medium.com/@yaroslavvb/tensorflow-meets-pytorch-with-eager-mode-714cce161e6c), by [Yaroslav Bulatov](https://medium.com/@yaroslavvb), 29 October 2017

## Source Code
* http://github.com/telecoms-intelligence/induction-pytorch-tensorflow

# Installation

## Python 3

### Ubuntu / Debian
```bash
$ sudo su -
$ apt-get -y install python3-dev python3-pip
```

### Fedora/CentOS/RedHat
* If needed, enable the EPEL repository
```bash
$ su -
$ yum -y install epel-release
```
* Install python34 and python-pip packages (but not virtualenv)
```bash
$ yum -y install python34 python-pip
```
* If needed, uninstall virtualenv
```bash
$ yum remove python-virtualenv
```
* Update pip and install virtualenv with pip
```bash
$ pip install --upgrade pip
$ pip install virtualenv
```

### MacOS
```bash
$ brew install python3
```

## Python virtual environment
* To install the Python 3 virtual environment:
```bash
$ pip install --upgrade pip
$ pip install virtualenv
$ mkdir ~/dev
$ cd ~/dev
$ virtualenv -p python3 venv3
```
* To activate the Python 3 virtual environment:
```bash
$ source ~/dev/venv3/bin/activate
```
* To deactivate the Python 3 virtual environment
```bash
$ deactivate
```

## PyTorch with the Eager execution engine

### On Linux
```bash
$ PF_ARCH="manylinux1"
```

### On MacOS
```bash
$ PF_ARCH="macosx_10_7"
```

### On all the platforms
```bash
$ source ~/dev/venv3/bin/activate
$ pip install -U pip
$ pip install http://download.pytorch.org/whl/cu80/torch-0.2.0.post3-cp36-cp36m-${PF_ARCH}.whl
$ pip install torchvision
$ pip install tf-nightly
```

# Walkthrough

```bash
$ source ~/dev/venv3/bin/activate
$ python python/kfac_nano_eager_test.py 
Step   0 loss 1.879871607
Step   1 loss 1.415868163
Step   2 loss 1.382389069
Step   3 loss 1.265281796
Step   4 loss 1.254014969
Step   5 loss 1.252885938
Step   6 loss 1.252338290
Step   7 loss 1.251988530
Step   8 loss 1.251742125
Step   9 loss 1.251557469
```

