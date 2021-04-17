解压
```sh
[root@master app]# tar -zxvf ~/Desktop/jdk-8u162-linux-x64.tar.gz -C /usr/local/[用户名，如lynx]/
[root@master app]# cd /usr/local/lynx/
[root@master lynx]# ls
jdk1.8.0_162
[root@master lynx]# pwd
/usr/local/lynx
[root@master lynx]# mv jdk1.8.0_162/ jdk
[root@master lynx]# pwd
/usr/local/lynx
[root@master lynx]# ls
jdk
[root@master lynx]# 
```
修改全局环境变量
```sh
[root@master bin]# vi /etc/profile
PATH=$PATH:$JAVA_HOME/bin
JAVA_HOME=/usr/local/lynx/jdk
export PATH JAVA_HOME
[root@master bin]# source /etc/profile
[root@master bin]# java -version
java version "1.8.0_162"
Java(TM) SE Runtime Environment (build 1.8.0_162-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.162-b12, mixed mode)
```
```sh
[root@master bin]# vim ~/.bashrc
export JAVA_HOME=/usr/local/lynx/jdk
[root@master bin]# source ~/.bashrc
[root@master bin]# echo $JAVA_HOME
[root@master bin]# java -version
[root@master bin]# echo $JAVA_HOME
```