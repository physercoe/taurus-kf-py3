Intro 简介
========
功夫是 [Taurus.ai](http://taurus.ai) 团队专为量化交易者设计的低延迟交易执行系统,代码原地址https://github.com/taurusai/kungfu
采用的python为2.7版本，原repository中也有pybind11分支实现python3的支持。本项目基于boost实现了python3的支持,较源代码改变较少。

开发环境：
Manjaro（arch)
boost 1.69
python 3.7.2


编译过程和原项目类似，使用 [CMake](https://cmake.org) 进行编译，

```
$ cd kungfu
$ mkdir build
$ cd build
$ cmake ..
$ make
$ make package
```

由于不是centos系统，没有yum，最后一步会报错，故最后需要手动安装：

```
$ cd _CPack_Packages/Linux/RPM/kungfu-1.0.0-Linux/opt
$ sudo cp -r kungfu /opt/
$ cd -
$ cd ../rpm/scripts
$ sudo ./post_install.sh
```



