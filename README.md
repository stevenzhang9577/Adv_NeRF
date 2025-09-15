# AdvNeRF: Generating 3D Adversarial Meshes With NeRF to Fool Driving Vehicles (IEEE TIFS 2025)
Official implementation of ["**[AdvNeRF: Generating 3D Adversarial Meshes With NeRF to Fool Driving Vehicles (IEEE TIFS 2025)](https://doi.org/10.1109/TIFS.2025.3609180)**"], **[Boyuan Zhang](https://scholar.google.com/citations?user=uBBaTjEAAAAJ&hl=en)**,**[Jiaxu Li](https://scholar.google.com/citations?user=annoZWEAAAAJ&hl=en)**, **[Yucheng Shi](https://scholar.google.com/citations?user=annoZWEAAAAJ&hl=en)**, **[YaHong Han](http://cic.tju.edu.cn/faculty/hanyahong/index.html)**, **[Qinghua Hu](https://scholar.google.com/citations?user=TVSNq_wAAAAJ&hl=en)**.
DOI: https://doi.org/10.1109/TIFS.2025.3609180


> **Abstract:** *The data fusion systems between multiple modals have attracted a wide range of concerns about their adversarial robustness. Recent image captioning attacks lack cross-structure transferability against models with diverse structures. Therefore, the attackers demonstrate satisfactory performance only when they gain full or partial knowledge of target image captioning models. So far, the cross-structure transferability of multi-modal adversarial examples has not been thoroughly investigated. In this paper, a theorem is proposed to analyze the upper bound captioning adversarial transferability. We design a new transfer-based adversarial attack method (Cascade & Allocate) against image captioning models. Our method can be divided into two steps. The first step randomly selects a set of candidate models with diverse structures, and we use a momentum-like strategy to generate perturbations. This ‘model cascade’ step narrows the gap of the gradient directions between different image captioning models, therefore enhancing the cross-model transferability and generating model-agnostic adversarial perturbations. The second step utilizes the upper bound transferability theorem to allocate the weight of perturbations per model. This ‘weight allocate’ step enhances the weight of model with the most consistent gradient in all candidate models, which generates more transferable adversarial examples. In the experiments, we compare our approach with other captioning and ensemble-based attacks against five blackbox models with different structures on MS COCO and Flickr-30k datasets. The adversarial examples exhibit state-of-the-art adversarial transferability against five black-box models with different structures. The results demonstrate that our approach is practical and generalizes well to a wide range of captioning models.*

### The codes will be released once they are annotated.


## 1. Method

<p align="center">
    <img src='/Framework.png' width=800/>
</p>

The framework of our AdvNeRF attack method. The generated 3D-targeted transferable adversarial mesh could attack the visual and LiDAR models at the same time.

## 2. Usage
### 2.1 Prepare data
The datasets used in the paper are available at the following links:
* [IM3D](https://github.com/Heathcliff-saku/VIAT)
* [Ori_NeRF](https://drive.google.com/drive/folders/1cK3UDIJqKAAm7zyrxRYVFJ0BRMgrwhh4)


### 2.2 Dependencies

* Python 3.11
* PyTorch 1.13.0
* numpy
* Pillow
* torchvision
* scipy

### 2.3 Train

```
python attack.py --device 0 --dataset MS_coco --models ./models --rounds 40 --model_number 5
```

## Citation
If you find our paper useful, please consider citing:
```
@ARTICLE{advnerf,
  author={Zhang, Boyuan and Li, Jiaxu and Shi, Yucheng and Han, Yahong and Hu, Qinghua},
  journal={IEEE Transactions on Information Forensics and Security}, 
  title={AdvNeRF: Generating 3D adversarial meshes with NeRF to fool driving vehicles}, 
  year={2025},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/TIFS.2025.3609180}}


```

