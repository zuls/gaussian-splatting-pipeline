# 3D Gaussian Splatting for Real-Time Radiance Field Rendering


This repository contains the official authors implementation associated with the paper "3D Gaussian Splatting for Real-Time Radiance Field Rendering", which can be found [here](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/). 


I have implemented this on my own datasets. 

Thanks

Quick Start

1. Activate the conda environment 
```
conda activate gaussian_splatting
```

2. Set the environment variables.
```
export CUDA_HOME=$CONDA_PREFIX
export PATH=$CUDA_HOME/bin:$PATH
export LD_LIBRARY_PATH=$CUDA_HOME/lib64:$LD_LIBRARY_PATH
export CC=$CONDA_PREFIX/bin/x86_64-conda-linux-gnu-gcc
export CXX=$CONDA_PREFIX/bin/x86_64-conda-linux-gnu-g++
```

3. Run training (ue GPU 1, 2 or 3 instead of default one 0)
```
CUDA_VISIBLE_DEVICES=1 python train.py -s tandt/train --iterations 7000

```


4. After training, Render images

```
CUDA_VISIBLE_DEVICES=1 python metrics.py -m ./output/<your_output_folder>

```



