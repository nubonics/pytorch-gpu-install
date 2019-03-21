[![Donate](https://img.shields.io/static/v1.svg?label=Donate&color=informational&message=PayPal)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=YUV3GZF22HZQC&source=url)
 </br>
[![Bitcoin](https://img.shields.io/static/v1.svg?label=Donate&color=informational&message=Bitcoin)](https://paxful.com/?r=zGMQymwDNQW)
3Mm7ueNMKpZdPX7t7ZWRXzKTfovLqrYCCT

# Pytorch GPU install instructions
At the end of these instructions you will have:   
1. A fully working conda environment running pytorch on GPUs

```bash
# create conda env
conda create -n torch python=3.6

# activate the created environment
conda activate torch

# install numpy
pip install numpy

# install torch (cuda 9)
conda install pytorch torchvision cuda90 -c pytorch

# if cuda 9 fails, install this way using cuda 8 
conda install pytorch torchvision -c pytorch
conda install cuda80 -c soumith

# test gpu install
python -c 'import torch; print(torch.rand(2,3).cuda())'
```
