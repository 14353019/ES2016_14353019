1.输入命令安装必要的环境
$	sudo apt-get update
$	sudo apt-get install ant
$ 	sudo apt-get install openjdk-7-jdk
$	sudo apt-get install unzip
2.下载关键的文件以待后面进行解压
Sudo wget 
http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz

sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip

3.新建dol的文件夹 
$	mkdir dol
将dolethz.zip解压到 dol文件夹中
$	unzip dol_ethz.zip -d dol
解压systemc
$	tar -zxvf systemc-2.3.1.tgz
4.编译systemc
解压后进入systemc-2.3.1的目录下
$	cd systemc-2.3.1
新建一个临时文件夹objdir
$	mkdir objdir
进入该文件夹objdir
$	cd objdir
运行configure(能根据系统的环境设置一下参数，用于编译)
$	../configure CXX=g++ --disable-async-updates
$	sudo make install
$	pwd
$	cd ../dol
$	ant -f build_zip.xml all
若成功会显示build successful
接着可以试试运行第一个例子
进入build/bin/mian路径下
$	cd build/bin/main
然后运行第一个例子
$	ant -f runexample.xml -Dnumber=1