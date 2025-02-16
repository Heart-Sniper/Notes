# Docker

+ 查看所有容器：`docker ps -a`
+ 启动容器：`docker start 容器名`
+ 停止容器：`docker stop 容器名`
+ 删除容器：`docker rm 容器名`
+ 创建容器并挂载目录和 GPU ：
  ```shell
  docker run -it --gpus all \
                --net=host \
                --name 容器名称 \
                -v 要挂载的宿主机目录:对应容器目录 \
                -w 容器的工作目录 \
                镜像名:tag /bin/bash
  ```
+ 进入容器：
  `docker exec -it 容器名 /bin/bash`

+ 查看容器内进程：
  `job -l`

+ 结束容器内进程：
  `kill -9 PID`

+ 昇腾 NPU 服务器上查找容器占用的 device:
  `docker inspect 容器名 | grep -i davinci`

## Jupyter with Docker

+ 容器内配置 Jupyter Notebook

  1. 容器内下载依赖包：`jupyter notebook`。
  2. 容器内运行 `jupyter notebook --generate-config`。
  3. 配置密码：容器内运行 `jupyter notebook password`。
  4. 进入步骤2中输出的路径的上层文件夹，进入.py配置文件，配置端口等参数。
  5. 容器内运行 `jupyter notebook --allow-root`, 复制输出的网址，挂起该终端不要退出。
  6. 将网址复制到 VS Code -> ipynb -> 选择内核。
   
+ 重新指定容器中的 Jupyter notebook 的环境路径：
  ```python
  import os
  os.chdir("所在路径")
  ```