# dockerfiles
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
