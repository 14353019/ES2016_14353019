1.�������װ��Ҫ�Ļ���
$	sudo apt-get update
$	sudo apt-get install ant
$ 	sudo apt-get install openjdk-7-jdk
$	sudo apt-get install unzip
2.���عؼ����ļ��Դ�������н�ѹ
Sudo wget 
http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz

sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip

3.�½�dol���ļ��� 
$	mkdir dol
��dolethz.zip��ѹ�� dol�ļ�����
$	unzip dol_ethz.zip -d dol
��ѹsystemc
$	tar -zxvf systemc-2.3.1.tgz
4.����systemc
��ѹ�����systemc-2.3.1��Ŀ¼��
$	cd systemc-2.3.1
�½�һ����ʱ�ļ���objdir
$	mkdir objdir
������ļ���objdir
$	cd objdir
����configure(�ܸ���ϵͳ�Ļ�������һ�²��������ڱ���)
$	../configure CXX=g++ --disable-async-updates
$	sudo make install
$	pwd
$	cd ../dol
$	ant -f build_zip.xml all
���ɹ�����ʾbuild successful
���ſ����������е�һ������
����build/bin/mian·����
$	cd build/bin/main
Ȼ�����е�һ������
$	ant -f runexample.xml -Dnumber=1