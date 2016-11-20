安装说明：
解压缩得到三个文件夹
OpenNI-Bin-Dev-Linux-x64-v1.5.7.10
NITE-Bin-Linux-x64-v1.5.2.23
Sensor-Bin-Linux-x64-v5.1.6.6
这三个包的版本是相互匹配的，注意ubuntu下不能使用openni2.2和NITE2.2版本的包

步骤：
1、安装openni
cd /home/siat/software/OpenNI-Bin-Dev-Linux-x64-v1.5.7.10
sudo ./install.sh
如果显示如下
Installing OpenNI
****************************

copying shared libraries...OK
copying executables...OK
copying include files...OK
creating database directory...OK
registering module 'libnimMockNodes.so'...OK
registering module 'libnimCodecs.so'...OK
registering module 'libnimRecorder.so'...OK
creating java bindings directory...OK
Installing java bindings...OK

*** DONE ***
则安装成功


2、安装NITE
cd /home/siat/software/NITE-Bin-Linux-x64-v1.5.2.23
sudo ./install.sh
如果显示如下：
Installing NITE
***************

Copying shared libraries... OK
Copying includes... OK
Installing java bindings... OK
Installing module 'Features_1_3_0'...
Registering module 'libXnVFeatures_1_3_0.so'... OK
Installing module 'Features_1_3_1'...
Registering module 'libXnVFeatures_1_3_1.so'... OK
Installing module 'Features_1_4_1'...
Registering module 'libXnVFeatures_1_4_1.so'... OK
Installing module 'Features_1_4_2'...
Registering module 'libXnVFeatures_1_4_2.so'... OK
Installing module 'Features_1_5_2'...
Registering module 'libXnVFeatures_1_5_2.so'... OK
Copying XnVSceneServer... OK
Installing module 'Features_1_5_2'
registering module 'libXnVHandGenerator_1_3_0.so'...OK
Installing module 'Features_1_5_2'
registering module 'libXnVHandGenerator_1_3_1.so'...OK
Installing module 'Features_1_5_2'
registering module 'libXnVHandGenerator_1_4_1.so'...OK
Installing module 'Features_1_5_2'
registering module 'libXnVHandGenerator_1_4_2.so'...OK
Installing module 'Features_1_5_2'
registering module 'libXnVHandGenerator_1_5_2.so'...OK
Adding license.. OK

*** DONE ***
则安装成功


3、安装Sensor
cd /home/siat/software/Sensor-Bin-Linux-x64-v5.1.2.1
sudo ./install.sh
如果显示如下
Installing PrimeSense Sensor
****************************

creating config dir /usr/etc/primesense...OK
copying shared libraries...OK
copying executables...OK
registering module 'libXnDeviceSensorV2KM.so' with OpenNI...OK
registering module 'libXnDeviceFile.so' with OpenNI...OK
copying server config file...OK
setting uid of server...OK
creating server logs dir...OK
installing usb rules...OK
installing modprobe blacklist...OK

*** DONE ***

则安装成功


4、运行示例
连上kinect的数据线
cd ~/software/OpenNI-Bin-Dev-Linux-x64-v1.5.7.10/Samples/Bin/x64-Release
./NiViewer 
如果出现kinect画面则配置成功


5、注意如果出现：
One or more of the following nodes could not be enumerated:

Device: PrimeSense/SensorV2/5.1.6.6: The device is not connected!
Device: PrimeSense/SensorV2/5.1.0.41: The device is not connected!
Device: PrimeSense/SensorV2/5.1.6.6: The device is not connected!
Device: PrimeSense/SensorV2/5.1.0.41: The device is not connected!

Press any key to continue . . .
这样的问题有可能是这三个包版本不匹配，我这里的三个包亲测是可用的。但是Sensor如果是5.1.6.6版本则出现上面报错。
