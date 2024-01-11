# linux 源码打包运行

## python3.11.6 安装教程
- 官网下载 python 版本，安装后配置环境变量，python -V 是 3.11.6，pip -V 是 23.0.1
    - [Download Gzipped source tarball](https://www.python.org/ftp/python/3.11.6/Python-3.11.6.tgz)
- 解压文件
```
tar -zxvf Python-3.11.6.tgz
```
- 创建文件夹
```
mkdir Python311
cd Python311
pwd #记住这里的路径
```
- 进入源码目录
```
 cd Python-3.11.6
```
- 配置源码，--prefix 是第二步骤 pwd 的绝对路径。
```
./configure --prefix="/home/jenkins/python/Python311" --enable-optimizations
```
- 等待配置
```
make && make install
```
- 设置环境变量
```
echo "export PATH=/home/jenkins/python/Python311/bin:$PATH">>~/.bashrc
```
- 执行生效
```
source ~/.bashrc
```

- 系统自带的 Python2 和 Python3 不要删除，也不要替换！
- 安装选项 --enable-shared 不要设置，没有/usr/lib 的权限，会失败
- --enable-optimizations 提高 Python 解释器的性能和执行效率
- 