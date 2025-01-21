# Nvdia_GPU_Setup
## Step 1: NVIDIA Video Driver
You should install the latest version of your GPUs driver. You can download drivers here:
https://www.nvidia.com/Download/index.aspx

## Step 2: Visual Studio C++
You will need Visual Studio, with C++ installed. By default, C++ is not installed with Visual Studio, so make sure you select all of the C++ options.
https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false

## Step 3: Anaconda/Miniconda
You will need anaconda to install all deep learning packages
https://www.anaconda.com/download/success

## Step 4: CUDA Toolkit
### Before downloading the CUDA Toolkit, check the latest version supported by your driver using the command below. Also, check the latest version supported by PyTorch using the link below.
#### open command prompt and run the below command
  nvidia-smi
#### Latest cuda supported by pytorch
https://developer.nvidia.com/cuda-toolkit-archive

### Download and installl toolkit:
https://developer.nvidia.com/cuda-toolkit-archive

## Step 5: download and install cuDNN:
https://developer.nvidia.com/rdp/cudnn-archive

## Step 6:
#### Copy the Application Extensions of bin lib and include from CuDNN and paste it to bin lib and include folder of NVIDIA GPU Computing Toolkit ( C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.4)

## Step 7: Check the environment variable path:
Variable Name: CUDA_PATH
Variable value: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.4

Variable Name: CUDA_PATH_V12_4
Variable value: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.4


## Step 8: Install PyTorch
https://pytorch.org/get-started/locally/

**Select the configuration. It will provide you the command to install Pytorch.
open command prompt and create a virtual environment and activate it and run the command given to install pytorch**

## Finally run the following script to test your GPU

import torch

print("Number of GPU: ", torch.cuda.device_count())
print("GPU Name: ", torch.cuda.get_device_name())

device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')
print('Using device:', device)






  
