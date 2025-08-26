<h1 align="center">🐳 Reproduce the results of MONAS-LQ within the container</h1>
-----------
-----------
## Overview

This container reproduces the results of MONAS-LQ, providing an environment for designing quantized CNNs for Automatic Modulation Classification with reduced computational cost.
It has been tested on Ubuntu 20.04 with brevitas 0.6.0 and onnx 1.7.0.

-----------
### Requirements
- Ubuntu 20.04+
- Docker
- GPU acceleration is supported, requiring the NVIDIA Container Toolkit installed on the host system.

-----------
## 2️⃣ Commands

### With GPU, direct connection to Jupyter
1️⃣
    - sudo docker build -t brevitas .

2️⃣
    - docker run --gpus all -it --rm \
      -p 8888:8888 \
      -v "$(pwd)":/workspace \
      -v "$(pwd)/sandbox":/workspace/sandbox \
      my-jupyterlab:pt1.7.1-cu110

3️⃣
- Open and run the code within the results.ipynb notebook.
