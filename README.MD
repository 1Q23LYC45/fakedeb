# FakeDEB
## 软件简介
本软件可以创建空的deb软件包。如果在安装deb文件某个依赖包不能安装，而这个依赖包并不是特别需要时，可以使用本软件伪造假依赖包文件。
## 安装方法
git clone https://github.com/1Q23LYC45/fakedeb
dpkg-deb --root-owner-group --build . 
dpkg -i ./..deb
rm ./..deb
## 使用方法
fakedeb <要伪造的软件名>
## 卸载
apt purge fakedeb
rm -rf /var/fakeutils