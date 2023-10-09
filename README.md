# Common CV

This project contains some problems we met when learning Computer Vision (CV), hope it can help you a lot!

Welcome to give your problems about CV in Issues and welcome to communicate with each other!

## Useful Tools
CUDAs

[Reference](https://segmentfault.com/a/1190000022561685)
[cuda-11.3](https://developer.nvidia.com/cuda-11.3.0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=18.04&target_type=runfile_local)

```
vim ~/.bashrc
source ~/.bashrc
sudo rm -rf /usr/local/cuda
sudo ln -s /usr/local/cuda-9.2 /usr/local/cuda
```

Face Parsing

[Reference](https://blog.csdn.net/weixin_43723625/article/details/116719701)

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

Q9. DISPLAY?
```
xeyes -display 192.168.196.104:0.0
sudo docker run --privileged --gpus all --name dlct3 -idt -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY docker_dlc:v1
```
