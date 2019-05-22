## ReadMe

### ./doc/ZTE_challenge_2019.pdf is the documentation of the methods I used in ZTE challenge preliminary



##### Firstly, you should add all of *.cu and *.cpp to src/caffe/layers, and add all of *.hpp to include/caffe/layers . Then， you need change the caffe.proto :

    message ConvolutionParameter {
	...
	optional bool combine_relu = 20 [default = false]; // add this sentence
	...
	}

then，recompile Caffe。

## How to use

<img src="https://ws1.sinaimg.cn/large/e2d9d843ly1g3addg0k4wj20m10g1q68.jpg" width=60%>

If you want to combine ReLU layer with convolutional layer (only on .caffemodel TEST stage), just delete ReLU layer directly and set `"combine_relu : true"` [default=False]。

## Some blogs about how to compile Caffe

### On Ubuntu

> [Ubuntu 16.04 下用 cmake 安装 caffe](https://blog.csdn.net/Chris_zhangrx/article/details/80867482)

### On windows

> [Windows 下用 build_win.cmd 直接编译CPU版caffe](https://blog.csdn.net/Chris_zhangrx/article/details/79096015)
> [Windows 下用 build_win.cmd 直接编译 GPU 版caffe](https://blog.csdn.net/Chris_zhangrx/article/details/83339684)
