# android_manifest
Android repo. (famod) - Manifest

-----------------------------------WIKI--------------------------------------------------------------------------
http://wiki.friendlyarm.com/wiki/index.php/NanoPC-T2/zh
编译Android

搭建编译环境
搭建编译Android的环境建议使用64位的Ubuntu 14.04，安装需要的包即可。
sudo apt-get install bison g++-multilib git gperf libxml2-utils make python-networkx zip
sudo apt-get install flex libncurses5-dev zlib1g-dev gawk minicom
更多说明可查看 https://source.android.com/source/initializing.html 。

下载源代码
Android源代码的下载需要使用repo，其安装和使用请查看 https://source.android.com/source/downloading.html 。
mkdir android && cd android
repo init -u https://github.com/friendlyarm/android_manifest.git -b nanopi2-lollipop-mr1
repo sync
其中“android”是指工作目录。

编译系统
source build/envsetup.sh
lunch aosp_nanopi2-userdebug
make -j8
-------------------------------------------------------------------------------------------------------------


http://pan.baidu.com/s/1dE8NySD#path=%252FNanoPi2%252Fsources 这是友善之臂提供是android源码包：
应该合并了google官方通用代码和“Android repo. (famod)”涉及的所有代码（https://github.com/friendlyarm?tab=repositories中。
具体通过android_manifest/default.xml搜索nanopi2涉及到的资源
