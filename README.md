# tensorflow-local-gpu
This repository is a guidance for using tensorflow in local machine with nvidia gpu (CUDA and cuDNN)

## Installation
1. Install [Anaconda](https://docs.anaconda.com/anaconda/install/windows/)
2. Install [Visual Studio Community](https://visualstudio.microsoft.com/downloads/) (Core Editor Only)
3. Install CUDA Toolkit and cuDNN that compatible with os machine and python version, respectively. (check compatibility : https://www.tensorflow.org/install/source#gpu)
4. Install [CUDA Toolkit 11.0 Update](https://developer.download.nvidia.com/compute/cuda/11.0.3/network_installers/cuda_11.0.3_win10_network.exe)
5. Download [cuDNN 8.0.5 for CUDA 11.0](https://developer.nvidia.com/rdp/cudnn-archive#a-collapse805-110)

   - Extract cuDNN zip file, copy all folders in `cuda` folder to `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0` (select replace)
   - Add these to `Path` environment variables

      ```cmd
      C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0\bin
      C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0\libnvvp
      C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0\extras\CUPTI\lib64
      C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0\include
      ```

   - Reboot

6. Create virtual environment
   - `conda create --name tf(version) python==3.8`
   - `conda activate tf(version)`
   - `pip install tensorflow==2.8.0`
   - `pip install opencv-python`
   - `pip install numpy`

7. Install Jupyter Notebook
   - `conda install -y jupyter`
   - `conda install -y nb_conda`
