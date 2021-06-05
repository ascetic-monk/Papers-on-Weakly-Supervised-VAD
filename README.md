# Papers-on-Weakly-Supervised-VAD
collect some papers on weakly-supervised Video Anomaly Detection.

## Papers
### 2018
[RWAD/Sultani.etl](http://openaccess.thecvf.com/content_cvpr_2018/papers/Sultani_Real-World_Anomaly_Detection_CVPR_2018_paper.pdf) Real-world Anomaly Detection in Surveillance Videos, CVPR 2018.

### 2019
[GCN-Anomaly](http://openaccess.thecvf.com/content_CVPR_2019/papers/Zhong_Graph_Convolutional_Label_Noise_Cleaner_Train_a_Plug-And-Play_Action_Classifier_CVPR_2019_paper.pdf) Graph Convolutional Label Noise Cleaner:Train a Plug-and-play Action Classifier for Anomaly Detection, CVPR 2019.

[TCN-IBL](https://ieeexplore.ieee.org/abstract/document/8803657/) Temporal Convolutional Network with Complementary Inner Bag Loss For Weakly Supervised Anomaly Detection. ICIP 2019.

[Motion-Aware](https://arxiv.org/pdf/1907.10211) Motion-Aware Feature for Improved Video Anomaly Detection. BMVC 19.

### 2020

[AR-Net](https://ieeexplore.ieee.org/document/9102722) Weakly Supervised Video Anomaly Detection via Center-Guided Discrimative Learning, ICME 2020.

[XD-Violence](https://arxiv.org/pdf/2007.04687.pdf) Not only Look, but also Listen: Learning Multimodal Violence Detection under Weak Supervision ECCV 2020.

[CLAWS](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123670358.pdf) CLAWS: Clustering Assisted Weakly Supervised Learning with Normalcy Suppression for Anomalous Event Detection ECCV 2020.


### 2021

[MIST](https://arxiv.org/abs/2104.01633) MIST: Multiple Instance Self-Training Framework for Video Anomaly Detection CVPR 2021.

[MTN-KMIL](https://arxiv.org/pdf/2101.10030.pdf) Weakly-supervised Video Anomaly Detection with Contrastive Learning of Long and Short-range Temporal Features Arxiv 2021.



## Preprocess & Feature Extractor

### Extract RGB and Flow Frames
Prepare the RGB and Flow frames ([link](https://github.com/yjxiong/temporal-segment-networks))(GCN-Anomaly)

### C3D
C3D-v1.0 CODE: default settings ([link](https://github.com/facebook/C3D))(RWAD/Sultani.etl)

C3D CODE: directly use the source codes from links. ([link](https://github.com/yjxiong/caffe/tree/3D))(GCN-Anomaly)

C3D MODEL: trained model on UCF. [baidu link](https://pan.baidu.com/s/1xmmlKYRu3Vd6FrzCeG1xng)password:9tq7(GCN-Anomaly)

### TSN
TSN CODE: directly use the source codes from links. ([link](https://github.com/yjxiong/temporal-segment-networks))(GCN-Anomaly)

C3D CODE: trained model on UCF. ([baidu link](https://pan.baidu.com/s/1xmmlKYRu3Vd6FrzCeG1xng)password:9tq7)(GCN-Anomaly)

### I3D
I3D FEATURES: [baidu link](https://pan.baidu.com/s/1Cn1BDw6EnjlMbBINkbxHSQ)(password: u4k6) or [google link](https://drive.google.com/file/d/193jToyF8F5rv1SCgRiy_zbW230OrVkuT/view?usp=sharing)(AR-Net)

I3D FEATURES: [ShangHai-train-onedrive-link](https://uao365-my.sharepoint.com/:f:/g/personal/a1697106_adelaide_edu_au/EiLi_oBQnAFCq3UG184p_akB2sV7szCWvOV9PtaKJ6lxtQ?e=MeM3TE), [ShangHai-test-onedrive-link](https://uao365-my.sharepoint.com/:f:/g/personal/a1697106_adelaide_edu_au/EvUUrWqpWqVHrXBzxbzAdD8BGiZBiumWWOaZmQ_AMAkAdg?e=P1rwCg), [ShangHai-train-google-link](https://drive.google.com/drive/folders/1L71Qa0gao6aLVhSjL0H-u2khmTRKcmQs?usp=sharing), [ShangHai-test-google-link](https://drive.google.com/drive/folders/1z-CQPpVtTyfZyPKZdv2hZ-h2oMF6s8ep?usp=sharing), [UCF-train-onedrive-link](https://uao365-my.sharepoint.com/:f:/g/personal/a1697106_adelaide_edu_au/ErCr6bjDzzZPstgposv1ttYBudL8UVnap6eHS46fFbooAQ?e=RZsMtA), [UCF-test-onedrive-link](https://uao365-my.sharepoint.com/:f:/g/personal/a1697106_adelaide_edu_au/EsmBEpklrShEjTFOWTd5FooBVXbeoDHTTqPZn60Vj3Guhg?e=hvv46w)(MTN-KMIL)


### Visual Feature Extraction
if you want to extract Visual Feature like this project, you can clone [this project](https://github.com/wanboyang/anomaly_feature)


## Performance on Dataset

### ShangHai Tech

|   Method    |First Author| Year | Conference |      Features       | 10-crop | GRAINED |  AUC   | FAR  |              |                                                              |
| :---------: | :-----: | :--: | :--------: | :-----------------: | :-----: | :-----: | :----: | ---- | ------------ | ------------------------------------------------------------ |
|    RWAD     | Sultani | 2018 |    CVPR    |       C3D-RGB       |    X    | Coarse  | 86.30  | 0.15 |              | Official(Keras)[code](https://github.com/WaqasSultani/AnomalyDetectionCVPR2018) |
|             |         |      |            |       I3D-RGB       |    √    | Coarse  | 85.33  |      | Re-implement |                                                              |
| GCN-Anomaly |  Zhong  | 2019 |    CVPR    |       C3D-RGB       |    √    |  Fine   | 76.44  |      |              | Official(Pytorch)[code](https://github.com/jx-zhong-for-academic-purpose/GCN-Anomaly-Detection) |
|             |         |      |            |      TSN-FLOW       |    √    |  Fine   | 84.13  |      |              |                                                              |
|             |         |      |            |       TSN-RGB       |    √    |  Fine   | 84.44  |      |              |                                                              |
|   TCN-IBL   |  Zhang  | 2019 |    ICIP    |       I3D-RGB       |         | Coarse  | 82.50  |      |              |                                                              |
|    CLAWs    | Zaheer  | 2020 |    ECCV    |       C3D-RGB       |         |         | 89.67  |      |              |                                                              |
|   AR-Net    |   Wan   | 2020 |    ICME    |       C3D-RGB       |         |  Fine   | 85.01* | 0.57 | Re-implement | Official(Pytorch)[code](https://github.com/wanboyang/Anomaly_AR_Net_ICME_2020) |
|             |         |      |            |      I3D Flow       |         |  Fine   | 82.32  |      |              |                                                              |
|             |         |      |            |       I3D-RGB       |         |  Fine   | 85.38  | 0.27 |              |                                                              |
|             |         |      |            | I3D-RGB & I3D  Flow |         |  Fine   | 91.24  | 0.10 |              |                                                              |
|    MTN-KMIL |  Tian   | 2021 |   arxiv    |       C3D-RGB       |    √    | Coarse  | 91.51  |      |              | Official(Pytorch)[Code](https://github.com/tianyu0207/MTN-KMIL) |
|             |         |      |            |       I3D-RGB       |    √    | Coarse  | 97.21  |      |              |                                                              |
|    MIST     |  Feng   | 2021 |    CVPR    |       C3D-RGB       |    X    |  Fine   | 93.13  | 1.71 |              | Official(Pytorch)[Code](https://github.com/fjchange/MIST_VAD)      |
|             |         |      |            |       I3D-RGB       |    X    |  Fine   | 94.83  | 0.05 |              |                                                              |


### UCF-Crime


|    Method    |First-Author| Year | Conference | Features | 10-crop | GRAINED |  AUC  | FAR  |              |                                                              |
| :----------: | :-----: | :--: | :--------: | :------: | :-----: | :-----: | :---: | :--: | ------------ | ------------------------------------------------------------ |
|     RWAD     | Sultani | 2018 |    CVPR    | C3D-RGB  |    X    |         | 75.41 | 1.9  |              | Official(Keras)[code](https://github.com/WaqasSultani/AnomalyDetectionCVPR2018) |
|              |         |      |            | I3D-RGB  |    X    |         | 77.92 |      |              |                                                              |
| GCN-Anomaly  |  Zhong  | 2019 |    CVPR    | C3D-RGB  |    √    |         | 81.08 | 2.2  |              | Official(Pytorch)[code](https://github.com/jx-zhong-for-academic-purpose/GCN-Anomaly-Detection) |
|              |         |      |            | C3D-RGB  |    X    |         | 80.67 | 3.3  | Re-implement |                                                              |
|              |         |      |            | TSN-FLOW |    √    |         | 78.08 |      |              |                                                              |
|              |         |      |            | TSN-RGB  |    √    |         | 82.12 |      |              |                                                              |
| Motion-Aware |   Zhu   | 2019 |    BMVC    | PWC Flow |         |         | 79.00 |      |              |                                                              |
|   TCN-IBL    |  Zhang  | 2019 |    ICIP    | C3D-RGB  |         |         | 78.66 |      |              |                                                              |
|    CLAWs     | Zaheer  | 2020 |    ECCV    | C3D-RGB  |    √    |         | 83.03 |      |              |                                                              |
| XD-Violence  |   Wu    | 2020 |    ECCV    | I3D-RGB  |    √    |         | 82.44 |      |              |                                                              |
|   MTN-KMIL   |  Tian   | 2021 |   arxiv    | C3D-RGB  |    √    | Coarse  | 83.28 |      |              | Official(Pytorch)[Code](https://github.com/tianyu0207/MTN-KMIL) |
|              |         |      |            | I3D-RGB  |    √    | Coarse  | 84.03 |      |              |                                                              |
|     MIST     |  Feng   | 2021 |    CVPR    | C3D-RGB  |    X    |  Fine   | 81.40 | 2.19 |              | Official(Pytorch)[Code](https://github.com/fjchange/MIST_VAD)  |
|              |         |      |            | I3D-RGB  |    X    |  Fine   | 82.30 | 0.13 |              |                                                              |

## Reference
Thanks for the conclusion from https://github.com/fjchange/awesome-video-anomaly-detection
