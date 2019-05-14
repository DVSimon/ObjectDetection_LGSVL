To build ROS2 packages:

```
docker-compose up build
```

Now, launch the lane following model:

```
docker-compose up drive
```


## Prerequisites

- Docker CE
- NVIDIA Docker
- NVIDIA graphics card (required for training/inference with GPU)



Uses shell of LGSVL Lane following script:

https://github.com/lgsvl/lanefollowing
