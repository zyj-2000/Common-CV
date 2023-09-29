# Ph.D-Experience
Eat, sleep and research
## Useful Tools
CUDAs

[cuda-11.3](https://developer.nvidia.com/cuda-11.3.0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=18.04&target_type=runfile_local)

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
