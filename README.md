# BraTS_2021_Challenge
BraTS 2021 Docker image 

Our docker image (https://hub.docker.com/repository/docker/parvezamu/tyagi_2023) can be used on BraTS 2018, BraTS 2019, BraTS 2020,  BraTS 2021 validation and testing datasets. 
Docker image can be downloaded using the command: docker pull parvezamu/tyagi_2023


It can be run for the outputs:

docker run --rm -v $HOME/input/:/input/ -v $HOME/output/:$HOME/output/  parvezamu/tyagi_2023
Contributions:
MS UNet used dense connections while enhancing the maximum features' size to 32 in the final output layer. Therefore, the number of features is twice that compared to the previous architecture {https://link.springer.com/chapter/10.1007/978-3-030-46643-5_15}. The output features at the levels of the encoder are 32, 64, 128, and 256. Inspired by the KiUNet {https://ieeexplore.ieee.org/document/9625988}, we redesigned strided convolutions in the encoder for high input resolution. MS UNet can be divided into (i) dense blocks, which are building blocks of the encoder-decoder, (ii) residual-inception blocks, which are used with the upsampling layers at the decoder, and (iii) deep supervision approach, which is proposed for faster convergence and better segmentation accuracy.


Acknowledgement:
Many thanks to the host of the BraTS and FeTS 2021 datasets.
Datasets can be downloaded:
1. BraTS 2018 (https://www.med.upenn.edu/sbia/brats2018/data.html) 
2.2019 (https://www.med.upenn.edu/cbica/brats2019/data.html) 
3. 2020 (https://www.med.upenn.edu/cbica/brats2020/data.html)
4. 2021 (https://www.kaggle.com/dschettler8845/brats-2021-task1). 
5. FeTS 2021 (https://zenodo.org/record/4573128).

