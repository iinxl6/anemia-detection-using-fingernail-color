# anemia-detector

Hybrid pipeline for non-invasive anemia detection from fingernail images, combining unsupervised feature learning (autoencoder + K-means pseudo-labeling) with supervised classifiers (SVM, Random Forest, ResNet50) on young and adult datasets. fileciteturn2file5L1-L7

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Datasets](#datasets)
* [Project Structure](#project-structure)
* [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
* [License](#license)

## Overview

Our study investigates non-invasive anemia detection through fingernail image analysis, leveraging two complementary publicly available datasets to improve model generalizability across age groups. fileciteturn2file12L28-L36

## Features

* **Autoencoder-based feature extraction** for unlabeled adult images
* **K-means++ pseudo-labeling** aided by PCA and scaling for clustering fileciteturn2file2L5-L13
* **Supervised classification** with SVM, Random Forest, and ResNet50 models
* **Hybrid workflow** seamlessly integrates unsupervised and supervised steps for robust performance

## Datasets

* **young dataset:** 4,260 clinically labeled fingernail images of children, balanced and preprocessed.
* **Adult dataset:** 750 unlabeled RGB hand images (18–95 years), with bounding-box metadata and pseudo-labels from clustering.

## Project Structure

```
anemia-detector/  
├── .gitignore               # Python artifacts, data caches
├── LICENSE                  # MIT License
├── README.md                # Project overview and setup instructions
├── environment.yml          # Conda environment file (or requirements.txt)
├── data/                    # Raw and processed data
│   ├── raw/                 # Original downloaded archives
│   └── processed/           # Cleaned and segmented images
├── notebooks/               # Jupyter notebooks for EDA and modeling
├── src/                     # Python modules for preprocessing, modeling, utils
└── reports/                 # Final PDF and Word reports
```

## Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/YourUsername/anemia-detector.git
   cd anemia-detector
   ```
2. Create the environment:

   ```bash
   conda env create -f environment.yml
   conda activate anemia-detector
   ```

## Usage

* **Exploratory analysis:** Open notebooks in `notebooks/` in Jupyter Lab.
* **Run training scripts:**

  ```bash
  python src/models/train_cnn.py  
  python src/models/train_svm_rf.py
  ```
* **Evaluate models:**

  ```bash
  python src/models/evaluate.py --model resnet50
  ```

## Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch: `git checkout -b my-feature`
3. Commit your changes: `git commit -m 'Add new feature'`
4. Push to branch: `git push origin my-feature`
5. Open a Pull Request

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
