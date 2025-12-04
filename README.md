<div align="center">
  <picture>
    <!-- User prefers dark mode: -->
  <source srcset="docs/en/_static/image/onedl-mmtracking-banner-dark.png"  media="(prefers-color-scheme: dark)"/>

<img src="docs/en/_static/image/onedl-mmtracking-banner.png" alt="OneDL-MMTracking logo" height="200"/>
  </picture>

<div>&nbsp;</div>
  <div align="center">
    <a href="https://vbti.nl">
      <b><font size="5">VBTI Website</font></b>
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://onedl.ai">
      <b><font size="5">OneDL platform</font></b>
    </a>
  </div>
<div>&nbsp;</div>

[![Docs](https://img.shields.io/badge/docs-latest-blue)](https://onedl-mmtracking.readthedocs.io/en/latest/)
[![license](https://img.shields.io/github/license/VBTI-development/onedl-mmtracking.svg)](https://github.com/VBTI-development/onedl-mmtracking/blob/main/LICENSE)

[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/onedl-mmtracking)](https://pypi.org/project/onedl-mmtracking/)
[![PyPI](https://img.shields.io/pypi/v/onedl-mmtracking)](https://pypi.org/project/onedl-mmtracking)

[![Build Status](https://github.com/VBTI-development/onedl-mmtracking/actions/workflows/merge_stage_test.yml/badge.svg)](https://github.com/VBTI-development/onedl-mmtracking/actions/workflows/merge_stage_test.yml)
[![Docker Image](https://github.com/VBTI-development/onedl-mmtracking/actions/workflows/docker.yml/badge.svg)](https://hub.docker.com/r/vbti/onedl-mmtracking-cu129-torch280)
[![open issues](https://isitmaintained.com/badge/open/VBTI-development/onedl-mmtracking.svg)](https://github.com/VBTI-development/onedl-mmtracking/issues)
[![issue resolution](https://isitmaintained.com/badge/resolution/VBTI-development/onedl-mmtracking.svg)](https://github.com/VBTI-development/onedl-mmtracking/issues)

[📘 Documentation](https://onedl-mmtracking.readthedocs.io/en/latest/) |
[🛠️ Installation](https://onedl-mmtracking.readthedocs.io/en/latest/get_started.html) |
[👀 Model Zoo](https://onedl-mmtracking.readthedocs.io/en/latest/model_zoo.html) |
[🆕 Update News](https://onedl-mmtracking.readthedocs.io/en/latest/notes/changelog.html) |
[🚀Ongoing Projects](https://github.com/vbti-development/onedl-mmtracking/projects) |
[🤔 Reporting Issues](https://github.com/VBTI-development/onedl-mmtracking/issues/new/choose) |

[![Discord Logo](https://cdn.prod.website-files.com/6257adef93867e50d84d30e2/66e3d80db9971f10a9757c99_Symbol.svg)](https://discord.gg/8DvcVRs5Pm)

</div>

## Introduction

OneDL MMTracking is an open source video perception toolbox by PyTorch.

The main branch works with **PyTorch2.8**.

<div align="center">
  <img src="https://user-images.githubusercontent.com/24663779/103343312-c724f480-4ac6-11eb-9c22-b56f1902584e.gif" width="800"/>
</div>

### Major features

- **The First Unified Video Perception Platform**

  We are the first open source toolbox that unifies versatile video perception tasks include video object detection, multiple object tracking, single object tracking and video instance segmentation.

- **Modular Design**

  We decompose the video perception framework into different components and one can easily construct a customized method by combining different modules.

- **Simple, Fast and Strong**

  **Simple**: MMTracking interacts with other OpenMMLab projects. It is built upon [MMDetection](https://github.com/open-mmlab/mmdetection/tree/3.x) that we can capitalize any detector only through modifying the configs.

  **Fast**: All operations run on GPUs. The training and inference speeds are faster than or comparable to other implementations.

  **Strong**: We reproduce state-of-the-art models and some of them even outperform the official implementations.

## What's New

The VBTI development team is reviving MMLabs code, making it work with
newer pytorch versions and fixing bugs. We are only a small team, so your help
is appreciated.

We release MMTracking 1.0.0rc0, the first version of MMTracking 1.x.

Built upon the new [training engine](https://github.com/open-mmlab/mmengine), MMTracking 1.x unifies the interfaces of datasets, models, evaluation, and visualization.

We also support more methods in MMTracking 1.x, such as [StrongSORT](https://github.com/open-mmlab/mmtracking/tree/dev-1.x/configs/mot/strongsort) for MOT, [Mask2Former](https://github.com/open-mmlab/mmtracking/tree/dev-1.x/configs/vis/mask2former) for VIS, [PrDiMP](https://github.com/open-mmlab/mmtracking/tree/dev-1.x/configs/sot/prdimp) for SOT.

Please refer to [dev-1.x](https://github.com/open-mmlab/mmtracking/tree/dev-1.x) branch for the using of MMTracking 1.x.

## Get Started

Please refer to [get_started.md](docs/en/get_started.md) for install instructions.

Please refer to [inference.md](docs/en/user_guides/3_inference.md) for the basic usage of MMTracking. If you want to train and test your own model, please see [dataset_prepare.md](docs/en/user_guides/2_dataset_prepare.md) and [train_test.md](docs/en/user_guides/4_train_test.md).

A Colab tutorial is also provided. You may preview the notebook [here](./demo/MMTracking_Tutorial.ipynb) or directly run it on [Colab](https://colab.research.google.com/github/open-mmlab/mmtracking/blob/master/demo/MMTracking_Tutorial.ipynb).

There are also usage [tutorials](docs/en/user_guides/), such as [learning about configs](docs/en/user_guides/1_config.md), [visualization](docs/en/user_guides/5_visualization.md), [analysis tools](docs/en/user_guides/6_analysis_tools.md),

## Benchmark and model zoo

Results and models are available in the [model zoo](docs/en/model_zoo.md).

### Video Object Detection

Supported Methods

- [x] [DFF](configs/vid/dff) (CVPR 2017)
- [x] [FGFA](configs/vid/fgfa) (ICCV 2017)
- [x] [SELSA](configs/vid/selsa) (ICCV 2019)
- [x] [Temporal RoI Align](configs/vid/temporal_roi_align) (AAAI 2021)

Supported Datasets

- [x] [ILSVRC](http://image-net.org/challenges/LSVRC/2017/)

### Single Object Tracking

Supported Methods

- [x] [SiameseRPN++](configs/sot/siamese_rpn) (CVPR 2019)
- [x] [MixFormer](configs/sot/mixformer) (CVPR 2022)
- [ ] [PrDiMP](https://arxiv.org/abs/2003.12565) (CVPR2020) (WIP)

Supported Datasets

- [x] [LaSOT](http://vision.cs.stonybrook.edu/~lasot/)
- [x] [UAV123](https://cemse.kaust.edu.sa/ivul/uav123/)
- [x] [TrackingNet](https://tracking-net.org/)
- [x] [OTB100](http://www.visual-tracking.net/)
- [x] [GOT10k](http://got-10k.aitestunion.com/)
- [x] [VOT2018](https://www.votchallenge.net/vot2018/)

### Multi-Object Tracking

Supported Methods

- [x] [SORT](configs/mot/sort) (ICIP 2016)
- [x] [DeepSORT](configs/mot/deepsort) (ICIP 2017)
- [x] [Tracktor](configs/mot/tracktor) (ICCV 2019)
- [x] [QDTrack](configs/mot/qdtrack) (CVPR 2021)
- [x] [ByteTrack](configs/mot/bytetrack) (ECCV 2022)

Supported Datasets

- [x] [MOT Challenge](https://motchallenge.net/)
- [x] [CrowdHuman](https://www.crowdhuman.org/)
- [x] [LVIS](https://www.lvisdataset.org/)
- [x] [TAO](https://taodataset.org/)
- [x] [DanceTrack](https://arxiv.org/abs/2111.14690)

### Video Instance Segmentation

Supported Methods

- [x] [MaskTrack R-CNN](configs/vis/masktrack_rcnn) (ICCV 2019)
- [x] [Mask2Former](configs/vis/mask2former) (CVPR 2022)

Supported Datasets

- [x] [YouTube-VIS](https://youtube-vos.org/dataset/vis/)

## Contributing

We appreciate all contributions to improve MMTracking. Please refer to [CONTRIBUTING.md](https://github.com/vbti-development/onedl-mmcv/blob/main/CONTRIBUTING.md) for the contributing guideline.

## Acknowledgement

OneDL-MMTracking is an open source project that welcome any contribution and feedback.
We wish that the toolbox and benchmark could serve the growing research
community by providing a flexible as well as standardized toolkit to reimplement existing methods
and develop their own new video perception methods.

## Citation

If you find this project useful in your research, please consider cite:

```latex
@misc{onedl-mmtrack2025,
    title={{OneDL MMTracking: OneDL Lab} video perception toolbox and benchmark},
    author={OneDL-MMTracking Contributors},
    howpublished = {\url{https://github.com/vbti-development/onedl-mmtracking}},
    year={2025}
}
```

## License

This project is released under the [Apache 2.0 license](LICENSE).

## Projects in VBTI-development

- [OneDL-MMEngine](https://github.com/vbti-development/onedl-mmengine): Foundational library for training deep learning models.
- [OneDL-MMCV](https://github.com/vbti-development/onedl-mmcv): Foundational library for computer vision.
- [OneDL-MMPreTrain](https://github.com/vbti-development/onedl-mmpretrain): Pre-training toolbox and benchmark.
- [OneDL-MMDetection](https://github.com/vbti-development/onedl-mmdetection): Detection toolbox and benchmark.
- [OneDL-MMRotate](https://github.com/vbti-development/onedl-mmrotate): Rotated object detection toolbox and benchmark.
- [OneDL-MMSegmentation](https://github.com/vbti-development/onedl-mmsegmentation): Semantic segmentation toolbox and benchmark.
- [OneDL-MMDeploy](https://github.com/vbti-development/onedl-mmdeploy): Model deployment framework.
- [OneDL-MIM](https://github.com/vbti-development/onedl-mim): MIM installs VBTI packages.
