# 源码打包运行

- 官网下载python版本，安装后配置环境变量，python -V 是3.11.6，pip -V 是 23.0.1
    - [Download Windows installer](https://www.python.org/ftp/python/3.11.6/python-3.11.6-amd64.exe)
    - [Download XZ compressed source tarball](https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tar.xz)
    - [Download Gzipped source tarball](https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tgz)
- 下载thingsboard-gateway版本，当前最新是 [3.4.4](https://codeload.github.com/thingsboard/thingsboard-gateway/zip/refs/tags/3.4.4)
- 安装依赖 
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
- 运行：进入build目录，执行 
```
python tb-gateway.py
```
- 执行的时候遇到提示升级，请勿升级！！！