Scheduler Performance Test
======

Steps to test performance of the official scheduler
------
- First you should have a go environment, the best practice is to run go in a docker environment. 

  ```dockerfile
  echo FROM golang:1.13.4 > Dockerfile
  docker build -t goenv:v1 .
  sudo docker run -it --privileged goenv:v1 /bin/bash
  ```

- Then you should be in a go docker

  ```
  git clone https://github.com/kubernetes/kubernetes
  make generated_files UPDATE_API_KNOWN_VIOLATIONS=true
  make UPDATE_API_KNOWN_VIOLATIONS=true
  cd test/integration/scheduler_perf/
  ./test-performance.sh
  ```

To make things more easier
------

 Docker image provided by [Veiasai](https://github.com/Veiasai) is a huge step toward the whole environment.

```shell
# get environment
docker pull registry.cn-shanghai.aliyuncs.com/veia/devkube
docker run -it registry.cn-shanghai.aliyuncs.com/veia/devkube /bin/bash
# do your work
cd kube/kubernetes
```

