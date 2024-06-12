Using the Dataset from https://www.synapse.org/Synapse:syn3193805/wiki/217789

The dataset was already preprocessed and downloaded from here:
https://drive.google.com/drive/folders/1ACJEoTp-uqfFJ73qS3eUObQh52nGuzCd

I'm  currently downloading the dataset from my Google Cloud in the current setup.

Setup:
Google Colab L4 GPU (Google Colab Subscription is needed)
Otherwise, you can just run the Jupyter Notebook after getting the dataset.

Currently it contains 3 different U-net architectures:
1) Basic one
2) U-net with 1 attention channel
3) U-net with double attention channel

There are 2 ways to evaluate at the end of the file:
1) Just calculation of the Hausdorff Distance and DSC
2) Calculation of Haursdorff Distance and DSC after applying CRF


References:
TransUNet: Transformers Make Strong Encoders for Medical Image Segmentation
Jieneng Chen, Yongyi Lu, Qihang Yu, Xiangde Luo, Ehsan Adeli, Yan Wang, Le Lu, Alan L. Yuille, Yuyin Zhou
PDF Link: https://arxiv.org/abs/2102.04306
Github Link: https://github.com/Beckschen/TransUNet

U-Net: Convolutional Networks for Biomedical Image Segmentation
Olaf Ronneberger, Philipp Fischer, Thomas Brox
https://arxiv.org/abs/1505.04597

Efficient Inference in Fully Connected CRFs with Gaussian Edge Potentials
PDF Link: https://arxiv.org/abs/1210.5644
Github Link: https://github.com/lucasb-eyer/pydensecrf
