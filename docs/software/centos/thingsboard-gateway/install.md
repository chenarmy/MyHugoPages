# 源码打包运行

## 前置条件
- 官网下载 python 版本，安装后配置环境变量，python -V 是 3.11.6，pip -V 是 23.0.1

    |  下载地址   | 安装教程  |
    |  ----  | ----  |
    | [Download Windows installer](https://www.python.org/ftp/python/3.11.6/python-3.11.6-amd64.exe)  | 暂无 |
    | [Download XZ compressed source tarball](https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tar.xz)  | 暂无 |
    | [Download Gzipped source tarball](https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tgz)  | [源码安装](../python3/install.md) |

- 下载 thingsboard-gateway 版本，当前最新是 [3.4.4](https://codeload.github.com/thingsboard/thingsboard-gateway/zip/refs/tags/3.4.4)
- 安装依赖 (windows 是 python 和 pip，linux 是 python3 和 pip3)
  
## 安装
- 安装依赖 (windows 是 python 和 pip，linux 是 python3 和 pip3)
```
pip install -r requirements.txt
```
- 安装：
```
python setup.py install
```
- 打包：
```
python setup.py build
```

## 运行
- 直接运行 
```
python thingsboard_gateway/tb-gateway.py
```
- 或者进入 build 目录，执行 
```
python tb-gateway.py
```
- 执行的时候遇到提示升级，请勿升级！！！
