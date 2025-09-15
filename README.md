# AdvNeRF: Generating 3D Adversarial Meshes With NeRF to Fool Driving Vehicles (IEEE TIFS 2025)
Official implementation of ["**[AdvNeRF: Generating 3D Adversarial Meshes With NeRF to Fool Driving Vehicles (IEEE TIFS 2025)](https://doi.org/10.1109/TIFS.2025.3609180)**"], **[Boyuan Zhang](https://scholar.google.com/citations?user=uBBaTjEAAAAJ&hl=en)**,**[Jiaxu Li](https://scholar.google.com/citations?user=annoZWEAAAAJ&hl=en)**, **[Yucheng Shi](https://scholar.google.com/citations?user=annoZWEAAAAJ&hl=en)**, **[YaHong Han](http://cic.tju.edu.cn/faculty/hanyahong/index.html)**, **[Qinghua Hu](https://scholar.google.com/citations?user=TVSNq_wAAAAJ&hl=en)**.
DOI: https://doi.org/10.1109/TIFS.2025.3609180


> **Abstract:** *Adversarial attacks on deep neural networks (DNNs) have raised significant concerns, particularly in safety-critical applications such as autonomous driving. Autonomous vehicles rely on both vision and LiDAR sensors to provide accurate 3D visual perception of their surroundings. However, adversarial vulnerabilities in these models pose several risks, as they can lead to misinterpretation of sensor data, ultimately endangering safety. While substantial research has been devoted to image-level adversarial attacks, these efforts are predominantly confined to 2D-pixel spaces, lacking physical realism and applicability in the 3D world. To address these limitations, we introduce AdvNeRF, a groundbreaking approach for generating 3D adversarial meshes that effectively target both vision and LiDAR models simultaneously. AdvNeRF is a Transferable Target Adversarial Attack that leverages Neural Radiance Fields (NeRF) to achieve its objectives. NeRF ensures the creation of high-quality adversarial objects and enhances attack performance by maintaining consistency across unseen viewpoints, making the adversarial examples robust from multiple angles. By integrating NeRF, our method represents a leap forward in improving the robustness and effectiveness of 3D adversarial attacks. Experimental results validate the superior performance of AdvNeRF, demonstrating its ability to degrade the accuracy of 3D object detectors under various conditions. These findings highlight the critical implications of AdvNeRF, emphasizing its potential to consistently undermine the perception systems of autonomous vehicles across different perspectives, thus marking an advancement in the field of adversarial attacks and 3D perception security.*

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

