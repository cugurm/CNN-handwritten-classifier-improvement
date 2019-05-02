# Offline_Writer_Identification
Code for paper, offline writer identification on character level <br>

# Datasets
## Nist Offline Handwritten Database (Manually pre-processed)
- [Nist by_class](https://drive.google.com/open?id=19lJdqYlnlyodhKIRLBuTKCN5EO30x4C4) <br>
- [Nist by_write](https://drive.google.com/open?id=1XI3XZZuj3BBMEescln8y_cQRjUE_-MiD) <br>
- [Processed ImageDisk](https://drive.google.com/open?id=17c2itFvFmpA0FUHiViYTpE3Nzc-B4YVU) (MNIST/EMNIST style preprocessed images, 28x28 pixels, grayscale) <br>
- [Processed InfoDisk](https://drive.google.com/open?id=1KLrAYpkMVKXRKrIRjW7pfA7-7KuGVArM) (Ground truth information about images and labels and writer ids) <br>

# Weights
## Nist weights
Weights are stored in separate folder NISTweights (baseline+finder) <br>

# src
## Nist
Source code consist of a couple of separate files: <br>
- **NIST_Data_Util.ipynb**                  - prepare dataset <br>
- **NIST_Data_Util_Advanced.ipynb**         - create ImageDisk and InfoDisk files <br>
- **NIST_Baseline_Training.ipynb**          - train baseline network and save weights and models (baseline+finder) <br>
- **NIST_Clustering_Knn_Evaluation.ipynb**  - cluster characters on train+val, create knn method and evaluate on final 200 writers (+2.36%) <br>

# NEW IDEAS:

## Parse UBuffalo inkmls
UBuffalo inkmls with writer identification parse it with CROHME tool 
HM: "Yes, the segGenerator.py script from crohmelib can do that. This is what we use to generate the isolated symbols from the full expressions (with ground-truth)."

- can't do that cause od mail conversation with Harlod Muchere - they have semi-supervised methond for character segmentation in Crohme

## ETH_Zurich dataset:
- [deepwriting_training.npz](https://drive.google.com/open?id=1bZLyuC8C8D8y94knKkpqbNrE7H76Yeki)<br>
- [deepwriting_validation.npz](https://drive.google.com/open?id=1MqYfcrdPDa9t8miWd4uj91gh_6ChTdG7)<br> are files in specific dictionary numpy format.

First convert them to:<br>
- [eth_dataset0.zip](https://drive.google.com/open?id=1oYEIGBxJ6BzmqCa0MD90OcTiPrXvVT5l) <br>
- [eth_dataset1.zip](https://drive.google.com/open?id=1baBXNqcmP9VGiC5BRruLrXqSCCfQxI-g) <br>
- [eth_dataset2.zip](https://drive.google.com/open?id=1-3EMwYauqJQAFeTV5pWHFiEKkSDGfs78) <br>
which are files in .svg format

Then onvert them to 28x28 centered, scale preserved .png images:<br>
- [ETH_png_archive.zip](https://drive.google.com/open?id=1RM9ZoXmnIwhIXNsngF73wj2ce-4CAy-A).
<br>
Wrchive contains 294 writers, 369455 images, average: 1256 images/writer
No of labels: 70
Average character / writer x label = 17.95 (Strongly unbalanced).
- Link to dataset on GoogleDrive: [Link](https://drive.google.com/open?id=1AdX4sndfOcl32B9CSWPn5VNDl4kW1hAP)

