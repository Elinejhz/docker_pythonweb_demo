# docker_pythonweb_demo
docker部署pythonweb环境，实现一个demo（For study use only）
搭建过程：
1、本地准备Dockerfile、docker-compose.yml、requirements.txt，以及demo运行的py文件
2、依次执行：
docker-compose config 根据docker-compose.yml解析后的配置信息；
docker-compose build 根据Dockerfile 构建容器环境；
docker-compose pull 拉取对应的镜像；
docker-compose up -d 启动镜像，依次执行Dockerfile中的配置信息；
docker-compose ps -a 查看容器信息
docker-compose top 查看启动中的容器进程信息
docker-compose start/restart 启动或重启容器
docker-compose stop 停止容器
