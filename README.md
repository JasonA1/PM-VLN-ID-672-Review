# A Priority Map for Vision-and-Language Navigation with Trajectory Plans and Feature-Location Cues

This repository contains source code and sample data for the priority map module (PM-VLN) and feature-location framework (FL<sub>PM</sub>) introduced in the paper "A Priority Map for Vision-and-Language Navigation with Trajectory Plans and Feature-Location Cues". The files presented here are intended to assist reviewers in assessing the methods and data detailed in the article and supplementary materials.


### Requirements
Python version >= 3.7

PyTorch version >= 1.8.0

Details of the Python packages required to run the code are listed in the following file:
requirements.txt

### Steps to Run the Framework
This repository contains source code and data samples to run the FL<sub>PM</sub> framework with the integrated PM-VLN. We tested and ran the code presented here on a single Tesla GPU with 16GB of RAM.


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
