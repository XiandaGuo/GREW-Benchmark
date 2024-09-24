## GREW-BENCHMARCH

This repository contains the code for our ICCV 2021 paper `Gait Recognition in the Wild: A Benchmark` 

## Getting Started

# [Apply for and Download](docs/0.download_datasets.md) GREW datasets.
# [Decompress and Organize](docs/1.decompress&organize_datasets.md) GREW datasets.


## Requirements

### Environment

1. Python 3.6.*
2. CUDA 11.1
3. PyTorch 
4. TorchVision 

### Install
Create a  virtual environment and activate it.
```shell
conda create -n grew python=3.6.12
conda activate grew
```
The code has been tested with PyTorch 1.0 and Cuda 11.1.
```shell
conda install pytorch=1.0.0 torchvision=0.2.1
conda install matplotlib tqdm
conda install tensorboard tensorboardX
conda install scipy scikit-image opencv
```
### Train
Train a model by
```bash
python train.py
```
- `--cache` if set as TRUE all the training data will be loaded at once before the training start.
This will accelerate the training.
**Note that** if this arg is set as FALSE, samples will NOT be kept in the memory
even if they have been used in the former iterations. #Default: TRUE

### Test
```bash
python build_submission.py
```
Participants must package the submission.csv for submission using zip xxx.zip $CSV_PATH and then upload it to [codalab](https://codalab.lisn.upsaclay.fr/competitions/3409).


## Acknowledgements

Part of the code is adopted from previous works: [GaitSet](https://github.com/AbnerHqC/GaitSet), We thank the original authors for their awesome repos.

Besides, some other attractive works extend the boundary of GREW.
- [DyGait](https://github.com/M-Candy77/DyGait)
- [SPOSGait](https://github.com/XiandaGuo/SPOSGait)

### Citing
If you find this code useful, please consider to cite our work.

```
@inproceedings{zhu2021gait,
    title={Gait Recognition in the Wild: A Benchmark},
    author={Zheng Zhu, Xianda Guo, Tian Yang, Junjie Huang, 
        Jiankang Deng, Guan Huang, Dalong Du,Jiwen Lu, Jie Zhou},
    booktitle={IEEE International Conference on Computer Vision (ICCV)},
    year={2021}              
}
@article{guo2022gait,
  title={Gait Recognition in the Wild: A Large-scale Benchmark and NAS-based Baseline},
  author={Guo, Xianda and Zhu, Zheng and Yang, Tian and Lin, Beibei and Huang, Junjie and Deng, Jiankang and Huang, Guan and Zhou, Jie and Lu, Jiwen},
  journal={arXiv e-prints},
  pages={arXiv--2205},
  year={2022}
}
```

## License
The GREW dataset is freely available for non-commercial use and may be redistributed under these conditions.
If you have any commercial questions, you can contact [Zheng Zhu](zhengzhu@ieee.org).
