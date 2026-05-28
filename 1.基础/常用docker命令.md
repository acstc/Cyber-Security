- 查看docker版本：docker -v
- 查看docker-compose版本：docker-compose -v
- 查看服务状态：systemctl status docker
- 查看镜像：docker images -a
- 下载镜像
  - docker pull library/hello-word:latest
  - library默认官方，可以省略  默认latest
- 删除镜像：sudo docker rmi ID号
- 启动镜像：docker run -itd --name=ubuntu id号 /bin/bash
- 列出容器
  - docker ps：正在运行的容器
  - docker ps -a：所有的容器
- 进入容器：docker exec -it 容器ID /bin/bash
- 停止容器：docker stop 容器ID
- 启动停止的容器：docker start 容器ID
- 删除容器：docker rm 容器ID
- 
- 
- 
- 

































































