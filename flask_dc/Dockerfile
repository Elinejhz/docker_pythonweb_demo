FROM python:3.8-alpine
LABEL maintainer="docker_pythonweb_test001"

#工作路径设为 /code
WORKDIR /code

#创建环境变量给Flask使用
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0

#复制 app.py到容器内 /code目录
COPY requirements.txt /code
COPY app.py /code

#安装gcc工具、python依赖
#RUN pip install flask && pip install redis
RUN python3 -m pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

#映射端口
EXPOSE 5000

STOPSIGNAL SIGTERM

#设置容器的默认启动命令
CMD [ "flask", "run" ]