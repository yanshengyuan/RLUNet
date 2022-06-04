# RLUNet
The Image Deblurring Network based on Local Self-Attention Feedback Connections proposed in my Master’s Thesis along with Ustormer.

The reason I propose RLUNet is that Ustormer’s performances on image deblurring is so bad that I need to find out a remedy for this task to let my thesis pass. RLUNet is different from the previous Pseudo_RLUNet that RLUNet’s reversed links from decoders to encoders are real. RLUNet works in a recurrent manner. The design of self-attention feedback connections refers to Hopfield network which is a classical Feedback Neural Network. Feedback Neural Network is contrary to Forward-Feeding Network. In Feedback Neural Network there are information flows from the last stages of the system to the early stage. RLUNet is actually a typical Feedback Neural Network designed based on U-net structure. RLUNet successfully achieves its expectations. Its performance on image deblurring is much better than Ustormer making my Master Thesis more perfect and more complete.

Illustrations for the use of this repository:

1, data preparation and training

First download GoPro dataset for training on GoPro's official site and run training command in below:

python3 ./train.py --arch Uformer --gpu '0,1,2,3,4,5,6,7' --train_ps 128 --train_dir ../GoPro/train --val_dir ../GoPro/test --embed_dim 16 --warmup --batch_size 64 --lr_initial 0.002 --nepoch 500

3, test and pretrained models

My originally pretrained weights will not be supplied here. When you have finished your own training, use your .pth files in the test.py scripts

If you want to use this repo for any academic or commercial purpose or if you have any questions to ask me please contact me in shengyuan_yan@163.com and for academic references please cite RLUNet as followings:

Shengyuan Yan. Research on Image Restoration Method based on Local Self-attention Mechanism[M]. Wuhan University, China, 2022.

Thanks for your attention and starring
