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
