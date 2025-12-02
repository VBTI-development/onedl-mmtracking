## Prerequisites

- Linux <del>| macOS | Windows</del>
- Python 3.10
- PyTorch 2.8
- CUDA 12.8+
- GCC 6+
- [OneDL-MMCV](https://onedl-mmcv.readthedocs.io/en/latest/get_started/installation.html)
- [OneDL-MMEngine](https://onedl-mmengine.readthedocs.io/en/latest/get_started/installation.html)
- [OneDL-MMDetection](https://onedl-mmdetection.readthedocs.io/en/latest/get_started.html#installation)

## Installation

### Detailed Instructions

1. Install [OneDL-MMDetection](https://onedl-mmdetection.readthedocs.io/en/latest/get_started.html#installation).

2. Install OneDL-MMTracking:
   a. From PyPI

   ```shell
   uv pip install onedl-mmtracking
   # if you want all optional dependencies, use:
   # mim install onedl-mmtracking[optional]
   ```

   b. From source

   ```shell
   git clone https://github.com/vbti-development/onedl-mmtracking.git
   cd onedl-mmtracking
   uv pip install -v -e .
   # "-v" means verbose, or more output
   # "-e" means installing a project in editable mode,
   # thus any local modifications made to the code will take effect without reinstallation.
   # if you want all optional dependencies, use:
   # pip install -v -e ".[optional]"
   ```

3. Install extra dependencies

- For MOT evaluation (required):

  ```shell
  uv pip install git+https://github.com/JonathonLuiten/TrackEval.git
  ```

- For VOT evaluation (optional)

  ```shell
  uv pip install git+https://github.com/votchallenge/toolkit.git
  ```

- For LVIS evaluation (optional):

  ```shell
  uv pip install git+https://github.com/lvis-dataset/lvis-api.git
  ```

- For TAO evaluation (optional):

  ```shell
  uv pip install git+https://github.com/TAO-Dataset/tao.git
  ```

### Developing with multiple MMTracking versions

The train and test scripts already modify the `PYTHONPATH` to ensure the script use the MMTracking in the current directory.

To use the default MMTracking installed in the environment rather than that you are working with, you can remove the following line in those scripts

```shell
PYTHONPATH="$(dirname $0)/..":$PYTHONPATH
```

## Verification

To verify whether MMTracking and the required environment are installed correctly, we can run **one of** MOT, VIS, VID and SOT [demo scripts](https://github.com/open-mmlab/mmtracking/blob/1.x/demo/):

Here is an example for MOT demo:

```shell
python demo/demo_mot_vis.py \
    configs/mot/deepsort/deepsort_faster-rcnn-r50-fpn_8xb2-4e_mot17halftrain_test-mot17halfval.py \
    --input demo/demo.mp4 \
    --output mot.mp4
```

If you want to run more other demos, you can refer to [inference guides](./user_guides/3_inference.md)
