# Papers-on-Weakly-Supervised-VAD
collect some papers on weakly-supervised Video Anomaly Detection.

## Papers
2018
[Sultani.etl](http://openaccess.thecvf.com/content_cvpr_2018/papers/Sultani_Real-World_Anomaly_Detection_CVPR_2018_paper.pdf) Real-world Anomaly Detection in Surveillance Videos, CVPR 2018.da
2019
[GCN-Anomaly] Graph Convolutional Label Noise Cleaner:Train a Plug-and-play Action Classifier for Anomaly Detection, CVPR 2019.
[IBL] Temporal Convolutional Network with Complementary Inner Bag Loss For Weakly Supervised Anomaly Detection. ICIP 19.
[Motion-Aware] Motion-Aware Feature for Improved Video Anomaly Detection. BMVC 19.
2020
[AR-Net] Weakly Supervised Video Anomaly Detection via Center-Guided Discrimative Learning, ICME 2020.
['XD-Violence'] Not only Look, but also Listen: Learning Multimodal Violence Detection under Weak Supervision ECCV 2020.
[CLAWS] CLAWS: Clustering Assisted Weakly Supervised Learning with Normalcy Suppression for Anomalous Event Detection ECCV 2020.
2021
[MIST] MIST: Multiple Instance Self-Training Framework for Video Anomaly Detection CVPR 2021 Project Page
[MTN-KMIL] Weakly-supervised Video Anomaly Detection with Contrastive Learning of Long and Short-range Temporal Features Arxiv 2021Code


## Performance on Dataset

### ShangHai Tech

|   Method    | Author  | Year | Conference |      Features       | 10-crop | GRAINED |  AUC   | FAR  |              |                                                              |
| :---------: | :-----: | :--: | :--------: | :-----------------: | :-----: | :-----: | :----: | ---- | ------------ | ------------------------------------------------------------ |
|             | Sultani | 2018 |    CVPR    |       C3D-RGB       |    X    | Coarse  | 86.30  | 0.15 |              | Official(Keras)[code](https://github.com/WaqasSultani/AnomalyDetectionCVPR2018) |
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
|    MIST     |  Feng   | 2021 |    CVPR    |       C3D-RGB       |    X    |  Fine   | 93.13  | 1.71 |              |                                                              |
|             |         |      |            |       I3D-RGB       |    X    |  Fine   | 94.83  | 0.05 |              |                                                              |


### UCF-Crime


|    Method    | Author  | Year | Conference | Features | 10-crop | GRAINED |  AUC  | FAR  |              |                                                              |
| :----------: | :-----: | :--: | :--------: | :------: | :-----: | :-----: | :---: | :--: | ------------ | ------------------------------------------------------------ |
|              | Sultani | 2018 |    CVPR    | C3D-RGB  |    X    |         | 75.41 | 1.9  |              | Official(Keras)[code](https://github.com/WaqasSultani/AnomalyDetectionCVPR2018) |
|              |         |      |            | I3D-RGB  |    X    |         | 77.92 |      |              |                                                              |
| GCN-Anomaly  |  Zhong  | 2019 |    CVPR    | C3D-RGB  |    √    |         | 81.08 | 2.2  |              | Official(Pytorch)[code](https://github.com/jx-zhong-for-academic-purpose/GCN-Anomaly-Detection) |
|              |         |      |            | C3D-RGB  |    X    |         | 80.67 | 3.3  | Re-implement |                                                              |
|              |         |      |            | TSN-FLOW |    √    |         | 78.08 |      |              |                                                              |
|              |         |      |            | TSN-RGB  |    √    |         | 82.12 |      |              |                                                              |
| Motion-Aware |   Zhu   | 2019 |    BMVC    | PWC Flow |         |         | 79.00 |      |              |                                                              |
|   TCN-IBL    |  Zhang  |      |            | C3D-RGB  |         |         | 78.66 |      |              |                                                              |
|    CLAWs     | Zaheer  | 2020 |    ECCV    | C3D-RGB  |    √    |         | 83.03 |      |              |                                                              |
|              |   Wu    | 2020 |    ECCV    | I3D-RGB  |    √    |         | 82.44 |      |              |                                                              |
|     MTN-KMIL |  Tian   | 2021 |   arxiv    | C3D-RGB  |    √    | Coarse  | 83.28 |      |              | Official(Pytorch)[Code](https://github.com/tianyu0207/MTN-KMIL) |
|              |         |      |            | I3D-RGB  |    √    | Coarse  | 84.03 |      |              |                                                              |
|     MIST     |  Feng   | 2021 |    CVPR    | C3D-RGB  |    X    |  Fine   | 81.40 | 2.19 |              |                                                              |
|              |         |      |            | I3D-RGB  |    X    |  Fine   | 82.30 | 0.13 |              |                                                              |

