#说明文档

-------

### 一、一键初始化环境

#### 1.安装包目的
>* 1、安装依赖包
>* 2、配置hosts
>* 3、卸载openjdk
>* 4、创建hadoop用户和组
>* 5、修改sshd_config文件，并重启sshd服务


#### 2.配置文件修改
>* 2.1.Init.conf
 1、想安装什么软件
 2、Root的密码
 3、是否配置新用户
>* 2.2.host.conf
 ip+空格+域名

> 192.168.56.151 master1
> 192.168.56.152 master1ha
> 192.168.56.153 master2
> 192.168.56.154 master2ha
> 192.168.56.155 h2slave1
> 192.168.56.156 h2slave2
> 192.168.56.157 h2slave3


#### 3.安装步骤
>* 1、将压缩包上传到linux的任意目录下（建议在/usr/local）
>* 2、解压
>* 3、进入initDir目录
>* 4、修改init.conf配置文件（如果有需要）
>* 5、修改host.conf文件（如果有需要）
>* 6、执行init.sh

------

### 二、一键安装ssh

#### 1、配置集群的ssh
#### 2、需要修改conf下的配置文件
>`INSTALL_USER="hadoop"`

安装用户
>`INSTALL_PASSWORD="hadoop"安装密码`
>` NODES="master1 master1ha master2 master2ha h2slave1 h2slave2 h2slave3"安装节点`
#### 3、执行bin下的installssh.sh


1、修改init文件下的init.conf文件
2、修改想要安装的其他节点，init/slaves
3、用root用户执行installProfileStart.sh初始化环境变量
4、用普通用户执行installSoft.sh，安装想安装的软件


------
### 三、一键安装软件


软件源地址：

> http://192.168.56.204/apache-flume-1.5.0-bin.tar.gz  
> http://192.168.56.204/hbase-0.99.2-bin.tar.gz         
> http://192.168.56.204/sqoop-1.4.4.bin__hadoop-1.0.0.tar.gz
> http://192.168.56.204/apache-hive-1.0.1-bin.tar.gz   
> http://192.168.56.204/kafka_2.8.0-0.8.0.tar.gz        
> http://192.168.56.204/zookeeper-3.4.5.tar.gz
> http://192.168.56.204/apache-storm-0.9.3.tar.gz      
> http://192.168.56.204/mahout-distribution-0.9.tar.gz
> http://192.168.56.204/hadoop-2.6.0.tar.gz            
> http://192.168.56.204/spark-1.5.2-bin-hadoop2.6.tgz
> http://192.168.56.204/jdk-7u71-linux-x64.tar.gz



------

参考内容:


>* [wangsenfeng/oneStepInstall  (https://github.com/wangsenfeng/oneStepInstall)](https://github.com/wangsenfeng/oneStepInstall)