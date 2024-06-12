Using the Dataset from https://www.synapse.org/Synapse:syn3193805/wiki/217789

The dataset was already preprocessed by Transunet paper creators and I downloaded it from here:
https://drive.google.com/drive/folders/1ACJEoTp-uqfFJ73qS3eUObQh52nGuzCd

I'm  currently downloading the dataset from my Google Cloud in the current setup.

**Setup:**
Google Colab L4 GPU (Google Colab Subscription is needed)

Otherwise, you can just run the Jupyter Notebook after getting the dataset from the link above.

Currently it contains 3 different U-net architectures:
1) Basic one
2) U-net with 1 attention gate
3) U-net with double attention gate

I saved each model after training, so you can just go straight to the testing portion of the assignment after uploading the model to Colab
1) unet_SCC_model.h5  ----  U-net run with just the Sparse Cross-Entropy Loss
2) unet_SGD_model.h5  ----  U-net run with Combined Loss = Dice Loss + Sparce Cross-Entropy Loss + using SGD optimizer (momentum=0.9, lr = 0.001)
3) unet_combined_Adam_model.h5 ---- U-net run with Combined Loss + Adam Optimizer (lr = 0.001)
4) unet_single_model.h5 ---- U-net run with Combined Loss + 1 attention gate + Adam Optimizer
5) unet_attention_model.h5 ---- U-net run with Combined Loss + double attention gate + Adam Optimizer

There are 2 ways to evaluate at the end of the file:
1) Just calculation of the Hausdorff Distance and DSC
2) Calculation of Haursdorff Distance and DSC after applying CRF

**References:**

1) **TransUNet: Transformers Make Strong Encoders for Medical Image Segmentation
Jieneng Chen, Yongyi Lu, Qihang Yu, Xiangde Luo, Ehsan Adeli, Yan Wang, Le Lu, Alan L. Yuille, Yuyin Zhou**

PDF Link: https://arxiv.org/abs/2102.04306

Github Link: https://github.com/Beckschen/TransUNet

2) **U-Net: Convolutional Networks for Biomedical Image Segmentation
Olaf Ronneberger, Philipp Fischer, Thomas Brox**

PDF Link: https://arxiv.org/abs/1505.04597

Github Link: https://github.com/milesial/Pytorch-UNet/tree/master/unet

3) **Efficient Inference in Fully Connected CRFs with Gaussian Edge Potentials
Philipp Krähenbühl, Vladlen Koltun**

PDF Link: https://arxiv.org/abs/1210.5644

Github Link: https://github.com/lucasb-eyer/pydensecrf

4) **Attention U-Net: Learning Where to Look for the Pancreas
Ozan Oktay, Jo Schlemper, Loic Le Folgoc, Matthew Lee, Mattias Heinrich, Kazunari Misawa, Kensaku Mori, Steven McDonagh, Nils Y Hammerla, Bernhard Kainz, Ben Glocker, Daniel Rueckert**

PDF Link: https://arxiv.org/abs/1804.03999
