- cd /home：切换目录/home

- mkdir /home/test：创建文件夹test

- touch  /home/1.txt：创建文件

- rm -rf：删除文件或文件夹  -r递归   -f强制

- cp 1.txt /home：复制文件或目录

- mv 1.txt /home：移动文件或目录或重命名

- vim 1.txt：查看文件1.txt    

  - i：输入模式
  - 默认：命令模式
  - esc：：末行模式 :q!  wq

- cat 1.txt：查看文件

- 相对路径：../../ 上两级目录

- 绝对路径：完整路径  /home/kali/Desktop/1.txt

- 文件权限

  - 属主User：文件创建者

  - 属组Group：与文件相关联的用户组

  - 其他Others：系统上所有其他用户

  - ls -l 或 ll：查看文件权限    

  - 10位权限 -rwxr-xr-x   主kali 组kali

    - -普通文件 d目录
    - r读 w写 x执行

    - 主rwx 组r-x 其他r-x
    - 数字表示 r=4 w=2 x=1  777rwxrwxrwx 755rwxr-xr-x 744rwxr--r--
    - chmod 755 1.txt：修改权限   chmod u+x  (u、g、o   +、-  w、x)

- 文件下载

  - git clone 链接：下载开源项目
  - wget 文件所在链接：下载单个文件

- 

- 

- 

- 

- 

- 

- 

- 