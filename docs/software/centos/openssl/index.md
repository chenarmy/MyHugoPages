# openssl 升级

查看当前 openssl 版本：
```
openssl version
```
或者进入 openssl 命令行：

```
OpenSSL> version
```
当前版本为 1.0.2k-fips，希望升级到 1.1.1s，
官网下载地址：https://www.openssl.org/source/openssl-1.1.1s.tar.gz
之后传到服务器上；
（如果有内源传到内源上，之后下载会更方便）

## 安装依赖
```
yum -y groupinstall "Development Tools"
```
解压缩安装包并进入
```
tar -xf openssl-1.1.1s.tar.gz
cd openssl-1.1.1s
```
此后
```
./config shared --prefix=/usr/local/openssl
```
其中--prefix 是指定安装目录的

编译安装：
```
make
make install
```
找到之前的 openssl
```
which openssl
```
此处是/usr/bin/openssl

覆盖创建软链接
```
ln -sf /usr/local/openssl/bin/openssl /usr/bin/openssl
```
然后设置动态库路径，
编辑/etc/ld.so.conf，添加：
```
/usr/local/openssl/lib
```
然后
```
ldconfig
```
最后再查看 openssl 版本已经升级
```
openssl version
```
所有命令：

```
cd /tmp/
wget https://mirrors.******.com/package/openssl/openssl-1.1.1w.tar.gz
tar xf openssl-1.1.1w.tar.gz
cd openssl-1.1.1w/
./config --prefix=/usr/local/openssl
make && make install
ln -s /usr/local/openssl/lib/libssl.so.1.1 /usr/lib64/libssl.so.1.1
ln -s /usr/local/openssl/lib/libcrypto.so.1.1 /usr/lib64/libcrypto.so.1.1
ln -sf /usr/local/openssl/bin/openssl /usr/bin/openssl
echo "/usr/local/openssl/lib" >> /etc/ld.so.conf
ldconfig
```