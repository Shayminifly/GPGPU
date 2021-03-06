# GPGPU: Detect Barcodes with CUDA
![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
[![made-with-cuda](https://img.shields.io/badge/Made%20with-CUDA-9cf?style=for-the-badge&logo=appveyor)](https://developer.nvidia.com/cuda-downloads)


This project is composed of:
* A CPU version
* A GPU version
* An improved GPU version (GPU_version2)

## How to run with docker
We created a docker image that is ready to compile and run cuda with openCV installed on it.
`docker-compose up -d`  
Then SSH to the docker: `docker exec -it gpgpu_dev_env /bin/bash`

### Exit docker
To quit the docker SSH: Ctrl+D  
Then: `docker-compose down`


## Make
We use Cmake. Go to the folder corresponding to the implementation you wish to use:  
`cd CPU_version` or `cd GPU_version` or `cd GPU_version2`
Then: `mkdir build && cd build`  
`cmake .. && make`  

## How to run
Put the images you wish to process in the `input_images` folder  
When you have done the make part: `./main`  
The images will be written inside the `output_images` folder  

## Benchmark
To run the benchmark: `nvprof ./main`

## Authors:
* Denjoy Segolene (Shayminifly)
* Le Helloco Quentin (Viri0x)
* Sharpin Etienne (atomesZ)
* Lacambra Laura (laura519)
