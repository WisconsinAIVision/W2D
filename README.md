# W2D

This repo is the official implementation of our CVPR 2022 paper ["The Two Dimensions of Worst-case Training and the Integrated Effect for Out-of-domain Generalization"]().

## Getting Started

### Data Preparation
* Downloader datasets (except NICO and CelebA datasets)
```
python3 -m domainbed.scripts.download \
       --data_dir=./domainbed/data
```
* Downloade CelebA dataset from [here]()
* Downloade clean NICO dataset (provided by ours) from [here]()
* The directory structures are discribed at [OoD-Bench](https://github.com/ynysjtu/ood_bench)

### Install

* Pytorch

### Launch a sweep

```
cd /ood_bench/DomainBed
bash sweep/"dataset_name"/run.sh launch ../datasets 0
```
* To change the training setting, modify the scripts under /ood_bench/DomainBed/sweep.
* If you have any questions about the scripts, more details are discribed at [OoD-Bench](https://github.com/ynysjtu/ood_bench) and [DomainBed](https://github.com/facebookresearch/DomainBed)

### View the results

```
python -m domainbed.scripts.collect_results\
       --input_dir="sweep_output_path"
```

## Authors

Contributors names and contact info

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details

## Acknowledgments
