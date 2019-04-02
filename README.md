# Offline_Writer_Identification
Code for paper, offline writer identification on character level

# Datasets
## Nist Offline Handwritten Database (Manually pre-processed)
Nist by_class: 
Nist by_writer:
Processed ImageDisk: (MNIST/EMNIST style preprocessed images, 28x28 pixels, grayscale)
Processed InfoDisk: (Ground truth information about images and labels and writer ids)

# Weights
## Nist weights
Weights are stored in separate folder NISTweights

# src
# Nist
Source code consist of a couple of separate files:
NIST_Data_Util.ipynb              - prepare dataset
NIST_Data_Util_Advanced.ipynb     - create ImageDisk and InfoDisk files
NIST_Baseline_Training.ipynb      - train baseline network and save weights and models (baseline+finder)
NIST_Clustering_Knn_Evaluation.ipynb  - cluster characters on train+val, create knn method and evaluate on final 200 writers (+2.36%)

