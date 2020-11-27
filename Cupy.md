
安装cupy-ERROR: Command errored out with exit status
官方解決方法:
https://docs.cupy.dev/en/latest/install.html#install-cupy


terminal
```
nvidia-smi
```
輸入尋找CUDA版本
更新pip之後輸入對應的CUDA版本安裝cupy
```
$ python -m pip install -U setuptools pip
```
| CUDA | center | 
| :--- | :--- | 
|v9.0|$ pip install cupy-cuda90|
|v9.2|$ pip install cupy-cuda92|
|v10.0|$ pip install cupy-cuda100|
|v10.1|$ pip install cupy-cuda101|
|v10.2|$ pip install cupy-cuda102|
|v11.0|$ pip install cupy-cuda110|
|v11.1|$ pip install cupy-cuda111|
