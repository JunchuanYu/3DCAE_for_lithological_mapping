3D autoencoder algorithm for lithological mapping using ZY-1 02D hyperspectral imagery: a case study of Liuyuan region
===================================================================

A hyperspectral image (HSI) contains hundreds of spectral bands, which provide detailed spectral information, thus offering an inherent advantage in classification. The successful launch of the Gaofen-5 and ZY-1 02D hyperspectral satellites has promoted the need for large-scale geological applications, such as mineral and lithological mapping (LM). In recent years, following the success of computer vision, deep learning methods have shown their advantage in solving the problem of hyperspectral classification. However, the combination of deep learning and HSI to solve the problem of geological mapping is insufficient. We propose a new 3D convolutional autoencoder for LM. A pixel-based and cube-based 3D convolutional neural network architecture is designed to extract spatial–spectral features. Traditional and machine learning methods are employed as competing methods, trained on two real hyperspectral datasets, and evaluated according to the overall accuracy, F1 score, and other metrics. Results indicate that the proposed method can provide convincing results for LM applications on the basis of the hyperspectral data provided by the ZY-1 02D satellite. Compared with traditional methods, the combination of deep learning and hyperspectral can provide more efficient and highly accurate results. The proposed method has better robustness than supervised learning methods and shows great promise under small sample conditions. As far as we know, this work is the first attempt to apply unsupervised spatial–spectral feature learning technology in LM applications, which is of great significance for large-scale applications.



[[Paper]](https://www.spiedigitallibrary.org/journalArticle/Download?urlId=10.1117%2F1.JRS.15.042610)
[[Code]](https://github.com/JunchuanYu/3DCAE_for_lithological_mapping)

<hr>

<div align=center><img src="./Figure/architecture.jpg?raw=True" width="700" > </div>

####  <center> Architecture of 3DCAE

<hr>

#### Dependencies
- Tensorflow==1.13.1
- Keras==2.2.4
- Gdal==2.4.1

<hr>

Specifics of the learning algorithm
-----------------------------------

The following are the details of the learning algorithm used:

* Parameter update algorithm used: [Adagrad](http://www.jmlr.org/papers/volume12/duchi11a/duchi11a.pdf)
	* Batch size: 200
	* Learning rate: 0.01

* Number of steps: until best validation performance
<hr>

#### CASIA-SURF validation score (ACER)


| Single-modal Model                 | Color  | Depth  | ir     |
| --------------------- | ------ | ------ | ------ |
| FaceBagNet            | 0.0672 | 0.0036 | 0.1003 |
| ConvMixer             | 0.0311 | 0.0025 | 0.1073 |
| MLPMixer              | 0.0584 | 0.0010 | 0.2382 |
| VisionPermutator(ViP) | 0.0570 | 0.0304 | 0.2571 |
| VisonTransformer(ViT) | 0.0683 | 0.0036 | 0.2799 |

| Multi-modal Model         | patch size 32 | patch size 48 | patch size 64 |
| ----------------- | ------------- | ------------- | ------------- |
| FaceBagNetFusion  | 0.0009        | 0.0006        | 0.0007        |
| ViTFusion         | 0.0169        | 0.0778        | 0.0375        |
<hr>

## Citation
If you find this work or code is helpful in your research, please cite:
```
Junchuan Yu, Liang Zhang, Qiang Li, Yichuan Li, Wei Huang, Zhiwei Sun, Yanni Ma, and Peng He "3D autoencoder algorithm for lithological mapping using ZY-1 02D hyperspectral imagery: a case study of Liuyuan region," Journal of Applied Remote Sensing 15(4), 042610 (20 September 2021). https://doi.org/10.1117/1.JRS.15.042610
```
#### Bibtex:
```
@article{10.1117/1.JRS.15.042610,
author = {Junchuan Yu and Liang Zhang and Qiang Li and Yichuan Li and Wei Huang and Zhiwei Sun and Yanni Ma and Peng He},
title = {{3D autoencoder algorithm for lithological mapping using ZY-1 02D hyperspectral imagery: a case study of Liuyuan region}},
volume = {15},
journal = {Journal of Applied Remote Sensing},
number = {4},
publisher = {SPIE},
pages = {1 -- 14},
keywords = {deep learning, lithological mapping, autoencoder, hyperspectral, small sample, ZY-1 02D, Hyperspectral imaging, 3D image processing, 3D modeling, Machine learning, Minerals, Associative arrays, Computer programming, Satellites, Data modeling, Spatial resolution},
year = {2021},
doi = {10.1117/1.JRS.15.042610},
URL = {https://doi.org/10.1117/1.JRS.15.042610}
}
```
<hr>

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
<hr>
