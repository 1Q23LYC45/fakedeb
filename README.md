# fakedeb
## 说明
本软件用于创建空的dpkg软件包。
可用于在dpkg出现依赖问题是，安装一些无法安装但可有可无的依赖包。
注意，软件生成的依赖包是假的，如果软件必须这个依赖，软件会无法运行。
## 安装方法
如果安装出错，请移动本README.MD到上级目录或删除本文件
git clone https://github.com/1Q23LYC45/fakedeb
chmod 0755 ./fakedeb/DEBIAN
chmod +x ./fakedeb/bin/fakedeb
dpkg-deb --root-owner-group --build ./fakedeb
dpkg -i fakedeb.deb
rm fakedeb.deb
## 用法
fakedeb <要伪装的软件名>
dpkg -i <生成的deb文件>
