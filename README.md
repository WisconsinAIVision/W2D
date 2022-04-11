# W2D

This repo is the official implementation of our CVPR 2022 paper ["The Two Dimensions of Worst-case Training and the Integrated Effect for Out-of-domain Generalization"]().

<p align="center">
 <img src="https://github.com/OoDBag/W2D/blob/main/overview.png" width="200" height="400" />


## Getting Started

### Data Preparation
* Downloader datasets (except NICO and CelebA datasets)
```
python3 -m domainbed.scripts.download \
       --data_dir=./domainbed/data
```
* Download CelebA dataset from [here]()
* Download clean NICO dataset (provided by ours) from [here]()
* The directory structures are discribed at [OoD-Bench](https://github.com/ynysjtu/ood_bench)

### Install

* Pytorch

### Launch a sweep

```
cd /ood_bench/DomainBed
bash sweep/"dataset_name"/run.sh launch ../datasets 0
```
* To change the training setting, modify the scripts under /ood_bench/DomainBed/sweep.
* If you have any questions about the scripts, more details are discribed at [OoD-Bench](https://github.com/ynysjtu/ood_bench) and [DomainBed](https://github.com/facebookresearch/DomainBed).
* Note: Since ResNet is not used in Colored_MNIST dataset, when you train on Colored_MNIST, comment line.   

### View the results

```
python -m domainbed.scripts.collect_results\
       --input_dir="sweep_output_path"
```

## Acknowledgments
The codebase is built upon [OoD-Bench](https://github.com/ynysjtu/ood_bench) and [DomainBed](https://github.com/facebookresearch/DomainBed).
