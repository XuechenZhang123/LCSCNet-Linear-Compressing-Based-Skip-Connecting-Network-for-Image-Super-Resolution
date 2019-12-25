# LCSCNet-Linear-Compressing-Based-Skip-Connecting-Network-for-Image-Super-Resolution
Codes for "LCSCNet: Linear Compressing Based Skip-Connecting Network for Image Super-Resolution", accepted by IEEE Transactions on Image Processing in 2019. 
## Abstract
In this paper, we develop a concise but efficient network architecture called linear compressing based skip-connecting network (LCSCNet) for image super-resolution. Compared with two representative network architectures with skip connections, ResNet and DenseNet, a linear compressing layer is designed in LCSCNet for skip connection, which connects former feature maps and distinguishes them from newly-explored feature maps. In this way, the proposed LCSCNet enjoys the merits of the distinguish feature treatment of DenseNet and the parameter- economic form of ResNet. Moreover, to better exploit hierarchical information from both low and high levels of various receptive fields in deep models, inspired by gate units in LSTM, we also propose an adaptive element-wise fusion strategy with multi- supervised training. Experimental results in comparison with state-of-the-art algorithms validate the effectiveness of LCSCNet.
## Train code
1. Download [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/) to 'dataset' file
2. Specify the parameter in 'src/demo.sh'. 
       For example, the scripts for BLCSCNet in the paper is 
### 
     python main.py --scale 2  --save  BELCSC_X2_B9U6 --model BELCSCNET --epochs 650 --batch_size 32 --loss '1*L1' --rate_list [0.75, 0.71875, 0.6875, 0.65625, 0.625, 0.59375, 0.5625, 0.53125, 0.5] --len_list [6, 6, 6, 6, 6, 6, 6, 6, 6]
