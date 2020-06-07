# Dockerfiles repository

This repo contains various different dockerfiles which help in Data Science workflows. 


## Dockerfile-torch-jupyter

This contains just the latest pytorch container and jupyter and jupyter lab. It is built for CPU, for testing locally. 

```
# build docker image
docker build -f <path-of-dockerfile> -t torch-jupyter:latest .

# run the image
docker run -it -p 8888:8888 -v $PWD:/src/ --name torchjupy torch-jupyter:latest
```	


## DeepLearning-CV-Dockerfile

This repo contains different dockerfiles which I require. Currently, there's just one dockerfile which is Deep Learning dockerfile for computer vision projects. It contains PyTorch, Tensorflow, Scikit, OpenCV and some other packages.   

Commands to use :   

```
# build docker image
nvidia-docker build -f <path-of-dockerfile> -t <name-of-docker-image>:<version-name> .

# find docker image id
nvidia-docker image ls

# run the image as container
nvidia-docker run --gpus all -it -p 8888:8888 -v /home/bhavulgauri/:/root/bhavulgauri <image-id>

# run jupyter inside the container
jupyter-lab --ip=0.0.0.0 --no-browser --allow-root --port=8888

# opening another terminal for container
nvidia-docker exec -it <container-id> /bin/bash
```
