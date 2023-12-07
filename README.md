# Common CV

This project contains some problems we met when learning Computer Vision (CV), hope it can help you a lot!

Welcome to give your problems about CV in Issues and welcome to communicate with each other!

## TMUX

```
tmux new-session -t projection
```

## Web

How to get the poste time of an URL?:
[Reference](https://mmys.club/how-to-find-the-published-date-of-a-web-page/#:~:text=%E6%9F%A5%E6%89%BE%E7%BD%91%E9%A1%B5%E5%8F%91%E5%B8%83%E6%97%A5%E6%9C%9F%E7%9A%84%206%20%E7%A7%8D%E6%96%B9%E6%B3%95%201%201.%20%E6%B5%8F%E8%A7%88%E7%BD%91%E9%A1%B5%20%E5%8F%91%E5%B8%83%E6%97%A5%E6%9C%9F%E6%98%AF%E5%9C%A8%E7%BA%BF%E5%88%9B%E5%BB%BA%E7%BD%91%E9%A1%B5%E6%89%80%E9%9C%80%E7%9A%84%E5%85%83%E6%95%B0%E6%8D%AE%E4%B9%8B%E4%B8%80%E3%80%82%20%E8%BF%99%E6%98%AF%E4%B8%80%E9%83%A8%E5%88%86,...%206%206.%20%E4%BD%BF%E7%94%A8%20Google%20%E6%9F%A5%E6%89%BE%E9%A1%B5%E9%9D%A2%E7%9A%84%E5%8F%91%E5%B8%83%E6%97%A5%E6%9C%9F%20%E5%A6%82%E6%9E%9C%E6%82%A8%E5%9C%A8%E4%B8%8A%E8%BF%B0%E6%96%B9%E6%B3%95%E4%B8%AD%E6%B2%A1%E6%9C%89%E6%89%BE%E5%88%B0%E9%A1%B5%E9%9D%A2%E7%9A%84%E5%8F%91%E5%B8%83%E6%97%A5%E6%9C%9F%EF%BC%8C%E9%82%A3%E4%B9%88%E8%B0%B7%E6%AD%8C%E5%8F%AF%E8%83%BD%E4%BC%9A%E5%B8%AE%E5%8A%A9%E6%82%A8%E6%89%BE%E5%88%B0%E5%AE%83%E3%80%82%20)

## Useful Tools
CUDAs

[Reference](https://segmentfault.com/a/1190000022561685)
[cuda-11.3](https://developer.nvidia.com/cuda-11.3.0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=18.04&target_type=runfile_local)

Codes in word/wps

[https://zhuanlan.zhihu.com/p/108483150](https://zhuanlan.zhihu.com/p/108483150)
```
vim ~/.bashrc
source ~/.bashrc
sudo rm -rf /usr/local/cuda
sudo ln -s /usr/local/cuda-9.2 /usr/local/cuda
```

Face Parsing

[Reference](https://blog.csdn.net/weixin_43723625/article/details/116719701)

Face Detector

[Reference](https://blog.csdn.net/woshicver/article/details/118586231)

## Some Concepts of Image Quality

**Bokeh (散景)** 景深较浅的摄影成像中，落在景深以外的画面，会有逐渐产生松散模糊的效果

**Chromatic Aberration （色差）** 指光学上透镜无法将各种波长的色光都聚焦在同一点上的现象，色差是由于镜头散射现象而造成的，图像中的物体周围特别是高对比度的情况下可能出现模糊或明显的色彩边缘（红、绿、蓝、黄、紫、洋红）就称之为色差

**Shallow depth-of-field (浅景深)**


## Common Problems
Q1. The Mathype in Word can't delete the formula:

Refer to [CSDN](https://blog.csdn.net/JGL121314/article/details/120868652)

Q2. The Problems occurred about xcb and MoTTY X11:
```
sudo apt-get install xvfb
xvfb-run pyhon xxx.py
```

Q3. The certificate expires when the mirror source is accessed:
```
sudo apt-get -o Acquire::https::mirrors.tuna.tsinghua.edu.cn::Verify-Peer=false install xxx
```

Q4. The source of pip
```
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

Q5. The connection of huggingface
```
# An example:
urllib3.exceptions.MaxRetryError: HTTPSConnectionPool(host='huggingface.co', port=443): Max retries exceeded with url: /api/models/runwayml/stable-diffusion-v1-5 (Caused by ConnectTimeoutError(<urllib3.connection.HTTPSConnection object at 0x7f8fc3db9990>, 'Connection to huggingface.co timed out. (connect timeout=None)'))
# Solution:
Find the corespingding model in huggingface:
https://huggingface.co/runwayml/stable-diffusion-v1-5/tree/main
```

Q6. Install OpenGL

Refer to [CSDN](https://blog.csdn.net/qq_40520596/article/details/111663646)

Q7. nvidia-smi: "Failed to initialize NVML: Driver/library version mismatch"
step 1. reboot
step 2. re install the driver of gpu
```
sudo apt-get purge nvidia*
sudo systemctl isolate multi-user.target
sudo modprobe -r nvidia-drm
sudo ./NVIDIA-Linux-x86_64-530.41.03.run
```

Q8. Dismatch between CUDA and Eigen3
Refer to [CSDN](https://blog.csdn.net/weixin_45736684/article/details/117512018)

Q9. TypeError: ‘numpy._DTypeMeta‘ object is not subscriptable
[CSDN](https://blog.csdn.net/qq_45878098/article/details/132815093)

Q10. DISPLAY?
```
xeyes -display 192.168.196.104:0.0
sudo docker run --privileged --gpus all --name dlct3 -idt -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY docker_dlc:v1
```

Q11. print(list) output is [] while len(list) is not zero.  
```
due to the list is [[], [], []……] so it's length is not zero but the print(list) is [].  
```

Q12.Codec between H264 and MPEG4
```
ffmpeg -i MPEG4.mp4 -vcodec h264 H264.mp4
```
