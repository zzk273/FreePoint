<br>
<p align="center">
<h1 align="center"><strong>FreePoint: Unsupervised Point Cloud Instance Segmentation</strong></h1>
  <p align="center">
    <a href='https://zzk273.github.io/' target='_blank'>Zhikai Zhang</a>&emsp;
    <a href='https://dingjiansw101.github.io/' target='_blank'>Jian Ding*</a>&emsp;
    <a href='https://llijiang.github.io/' target='_blank'>Li Jiang</a>&emsp;
    <a href='https://scholar.google.co.uk/citations?user=T51W57YAAAAJ&hl=en' target='_blank'>Dengxin Dai</a>&emsp;
    <a href='https://scholar.google.com/citations?user=SAUCVsEAAAAJ&hl=zh-CN' target='_blank'>Gui-Song Xia*</a>&emsp;
    <br>
    Wuhan University&emsp;KAUST&emsp;CUHK-Shenzhen&emsp;Huawei Zurich Research Center
  </p>
</p>

# News 🔥
- [2024-02] [FreePoint](https://arxiv.org/abs/2305.06973) is accepted by CVPR 2024. Thanks for the recognition!

# TODOs
- [x] Release class-agnostic instance segmentation training codebase
- [ ] Release pretrained checkpoints

# Prepare
Please refer to [Mask3D](https://github.com/JonasSchult/Mask3D) for detailed dataset and environment preparation.

## Code Structure
We adapt the codebase of [Mask3D](https://github.com/JonasSchult/Mask3D) and [Mix3D](https://github.com/kumuji/mix3d), which provide a highly modularized framework for 3D Segmentation based on the MinkowskiEngine.

```
FreePoint
│   ├── main_instance_segmentation_freepoint.py <- the main file
│   ├── conf                          <- hydra configuration files
│   ├── datasets
│   │   ├── preprocessing             <- folder with preprocessing scripts
│   │   ├── semseg_freepoint.py                 <- indoor dataset
│   │   └── utils_freepoint.py        
│   ├── models                        <- Mask3D modules
│   ├── trainer
│   │   ├── __init__.py
│   │   └── trainer.py                <- train loop
│   └── utils
├── data
│   ├── processed                     <- folder for preprocessed datasets
│   └── raw                           <- folder for raw datasets
├── scripts                           <- train scripts
├── docs
├── README.md
└── saved                             <- folder that stores models and logs
```

## Dependencies:
The main dependencies of the project are the following:
```yaml
python: 3.10.9
cuda: 11.3
```

# BibTex
If you find this repository helpful, please cite our work:

```bibtex
@inproceedings{zhang2024freepoint,
  title={Freepoint: Unsupervised point cloud instance segmentation},
  author={Zhang, Zhikai and Ding, Jian and Jiang, Li and Dai, Dengxin and Xia, Guisong},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={28254--28263},
  year={2024}
}
```