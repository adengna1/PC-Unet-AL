# PC-Unet-AL
PC-Unet-AL

This is the implementation for “PC-Unet-AL” for paper: “Active Learning-Enhanced Pyramidal Convolution Unet for Change Detection in Optical and SAR Remote Sensing Image Pairs”, on IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing (https://ieeexplore.ieee.org/abstract/document/10685129)

1. Dataset
To evaluate the performance of our PC-Unet-AL approach, we carry out a set of experiments utilizing three optical and SAR image pair datasets.

The first dataset, referred to as the Shuguang dataset, comprises a SAR image and an optical satellite image, depicted in Fig. 3 (a) and (b), respectively. The SAR image, measuring 593×921 pixels with a single channel, was captured by the Radarsat-2 using C-band technology in June 2008. The optical image, measuring 593×921 pixels with three channels, was obtained from Google Earth in September 2012, incorporating RGB bands. This dataset illustrates alterations in land use within farmland. The corresponding CM, depicted in Fig. 3(c), was meticulously annotated through a blend of prior information and expert knowledge.

Fig. 3. The Shuguang dataset. (a) Pre-changed image, (b) post-changed images, (c) the corresponding change map.

The second dataset, recorded as the California dataset, contains a multispectral image and a SAR image. The multispectral image, with dimensions of 3500×2000 pixels and 11 channels, was obtained by Landsat 8 on January 5, 2017. It consists of nine channels spanning from deep blue to shortwave infrared, along with two long-wave infrared channels (only RGB channels shown in Fig. 4 (a)). The SAR image was acquired by Sentinel-1A on February 18, 2017, covering the same area affected by a flood. This image has dimensions of 3500×2000 pixels and three channels, including two polarizations: VV and VH. Additionally, the dataset is enriched by incorporating a third channel that represents the ratio between the intensities of the two polarizations. All channels in the SAR image have undergone a log transformation. Its false color RGB image is displayed in Fig. 4 (b). The CM, annotated by Luppino et al. [1], is shown in Fig. 4(c). It illustrates the extent of flooding in California, USA.

Fig. 4. The California dataset. (a) Pre-changed image, (b) post-changed images, (c) the corresponding change map.

The third dataset, named the Gloucester dataset, depicts the changes in the area before and after a flooding event in Gloucester, England. It comprises an optical image and a SAR image, as illustrated in Fig. 5 (a) and (b), respectively. The optical image, measuring 2325×4135 pixels with three channels, was captured by Quickbird-2 in July 2006. The SAR image, with dimensions of 2325×4135 pixels and a single channel, was obtained from TerraSAR-X in July 2007. The original CM for this dataset [2], as shown in Fig. 5 (c), was meticulously created through a manual process that involved integrating prior information and leveraging expert knowledge. However, after conducting a careful examination of the pre-event optical image (Fig. 5 (a)) and the post-event SAR image (Fig. 5 (b)), we have discovered that the original ground truth (Fig. 5 (c)) unintentionally overlooked certain areas of change, as indicated by the red rectangular box. Consequently, we have annotated these previously omitted changed regions and created a revised CM for this dataset, as depicted in Fig. 5 (d). For the subsequent experiments, we have utilized the revised CM to conduct our analysis.

Fig. 5. The Gloucester dataset. (a) Pre-changed image, (b) post-changed images, (c) the original change map, (d) the revised change map.

Reference：

[1] L. T. Luppino, F. M. Bianchi, G. Moser, and S. N. Anfinsen, "Unsupervised Image Regression for Heterogeneous Change Detection," IEEE Transactions on Geoscience and Remote Sensing, vol. 57, no. 12, pp. 9960-9975, 2019.

[2] R. Touati and M. Mignotte, "An energy-based model encoding nonlocal pairwise pixel interactions for multisensor change detection," IEEE Transactions on Geoscience and Remote Sensing, vol. 56, no. 2, pp. 1046-1058, 2017.
