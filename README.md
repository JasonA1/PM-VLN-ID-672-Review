# A Priority Map for Vision-and-Language Navigation with Trajectory Plans and Feature-Location Cues

This repository contains source code and sample data for the priority map module (PM-VLN) and feature-location framework (FL<sub>PM</sub>) introduced in the paper "A Priority Map for Vision-and-Language Navigation with Trajectory Plans and Feature-Location Cues". The files presented here are intended to assist reviewers in assessing the methods and data detailed in the article and supplementary materials.


### Requirements
Python version >= 3.7

PyTorch version >= 1.8.0

Details of the Python packages required to run the code are listed in the following file:
requirements.txt

### Steps to Run the Framework
This repository contains source code and data samples to run the FL<sub>PM</sub> framework with the integrated PM-VLN. We tested and ran the code presented here on a single Tesla GPU with 16GB of RAM.

- CD into the main directory.
- Install requirements for the project: pip install -r requirements.txt
- Untar the tar archive containing the datasets (see below): tar -xzvf datasets_paper_id_672.tar.gz
- Start training and evaluation:

``` bash
# clone the repository
python main.py --dataset vln_sl_sample --img_feat_dir ./datasets/vln_sl_sample/features/ --pt_feat_dir ./datasets/vln_sl_sample/pt_features/ --hidden_dim 256 --model vbforvln --vln_batch_size 2 --fl_batch_size 5 --max_num_epochs 1 --exp_name train_tini_new --store_ckpt_every_epoch True --fl_dir datasets/mc_10_sample --fl_dataset mc_10 --fl_feat_dir datasets/mc_10_sample/features --fl_pt_feat_dir datasets/mc_10_sample/pt_features --max_instr_len 180 --max_window_len 80 --max_t_v_len 140
```

### Data
#### Data Samples
Data for review are submitted in the following tar archive uploaded with supplementary material: datasets_paper_id_672.tar.gz

This file contains directories with two types of dataset: 
* Samples from datasets introduced in this research for manual review:
  - mc_10_subset - JSON file and 5 sample images of entities from the MC-10 dataset.
  - tr_ny_pit_subset - JSON and 5 sample images of path traces from the TR-NY-PIT-central dataset.
* Sample data to run the framework:
  - mc_10_sample - data from MC-10 to train the PM-VLN module.
  - vln_sl_sample - sample VLN dataset containing nine modified samples of routes from StreetLearn. 

#### Touchdown
In order to access and download Touchdown and StreetLearn, please refer to this link:
https://sites.google.com/view/streetlearn/touchdown
