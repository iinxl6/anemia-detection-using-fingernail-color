# anemia-detector

Hybrid pipeline for non-invasive anemia detection from fingernail images, combining unsupervised feature learning (autoencoder + K-means pseudo-labeling) with supervised classifiers (SVM, Random Forest, ResNet50) on young and adult datasets. 

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Datasets](#datasets)
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

- **Children fingernail images**  
  Source: [Mendeley Data – Fingernails](https://data.mendeley.com/datasets/2xx4j3kjg2/1)  
  Cite as:
  > “Asare, Justice Williams; APPIAHENE, PETER; DONKOH, EMMANUEL (2022), “Detection of Anemia using Colour of the Fingernails Image Datasets from Ghana”, Mendeley Data, V1, doi: 10.17632/2xx4j3kjg2.1”

- **Adult fingernail images (preprocessed)**  
  Source: [GitHub – TasBakker/Anemia-Detection: `dataset_fingernails`](https://github.com/TasBakker/Anemia-Detection/tree/main/dataset_fingernails)  
  Cite as:  
  > TasBakker (2024), *Anemia-Detection: dataset_fingernails* [GitHub repository], https://github.com/TasBakker/Anemia-Detection/tree/main/dataset_fingernails (accessed August 6, 2025).  
  > Original dataset by Yakimov, B.; Buiankin, K.; Denisenko, G.; Bardadin, I.; Shitova, Y.; Shirshin, E. (2024), “Dataset of human skin and fingernails images for non-invasive haemoglobin level assessment”, figshare. Collection. https://doi.org/10.6084/m9.figshare.c.6760179


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
