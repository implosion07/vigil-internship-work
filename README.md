# Brain Tumor Detection Research Project

This repository contains the work executed during my research internship at VIGIL labs of IIT Hyderabad. The research focused on establishing similarities between brain tumor detection datasets and implementing various methods for information extraction and dataset comparison.

## Datasets

The datasets used for this investigation were related to Brain Tumour Detection and can be downloaded from Kaggle using the links below:

* Source dataset: [Brain Tumor Detection](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection)
* Target dataset: [Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)

## Project Overview

The aim of this internship was primarily to study methods for establishing similarities between two given datasets and implementing approaches to gain a better understanding of the datasets. This research addresses the common issue of limited specialized data available for specific tasks, in contrast to the large amount of generalized data that is more readily available.

## Project Structure

```
brain-tumor-research/
├── main.ipynb                  # Main implementation notebook
├── README.md                   # Project documentation
```

## Implementation Details

The notebook titled **main.ipynb** contains the following implementations:

1. **Summary and Visualization of the two datasets**
   - Viewing images present in each class
   - Reading images and corresponding labels
   - Computing mean images from each class
   - Computing standard deviation images from each class
   - Visualization of random images and labels
   - Principal Component Analysis to summarize the image data

2. **Gradient-based Class Activation Mapping (Grad-CAM)**
   - Implementation on both brain tumor datasets
   - Technique to visualize discriminative image regions used by CNN models
   - Class-specific visualizations showing which regions are relevant to classification

3. **Autoencoder Average Distance (AAD)**
   - Converting dataset images into numeric vectors
   - Computing the difference between the average of vectors in each dataset
   - Determining similarity between the two brain tumor datasets

The implementation steps for AAD included:
- Creating arrays for Source and Target Dataset
- Creating an Autoencoder and providing it with arrays from both datasets
- Producing the required vectorized metrics
- Determining the average of the vectors
- Computing the difference between the average vectors to determine the AAD

## Additional Research Topics

In addition to the implementations included in this repository, the following topics were studied during the internship (code not provided):

1. **Grad-CAMs on Office31 Dataset**
   - Applied visualization techniques to a different domain adaptation dataset

2. **Optimal Transport Theory**
   - Used to find the distance between the two datasets
   - Mathematical framework for comparing probability distributions

3. **Direct Domain Adaptation**
   - Methods to find similarities between the two datasets
   - Techniques for transferring knowledge between domains

## Running the Code

### Prerequisites

The following packages are required to run the code:

```
tensorflow>=2.4.0
keras>=2.4.3
numpy>=1.19.5
pandas>=1.2.0
matplotlib>=3.3.3
scikit-learn>=0.24.0
pillow>=8.1.0
opencv-python>=4.5.1
jupyter>=1.0.0
```

You can install all required packages using:

```bash
pip install -r requirements.txt
```

### Dataset Setup

1. Download the datasets from the provided Kaggle links
2. Ensure the directory structure follows the expected format as outlined in the code

### Running the Notebook

The main notebook can be executed in two ways:

#### Using Jupyter Notebook

```bash
jupyter notebook main.ipynb
```

#### Using Google Colab

1. Upload the notebook to Google Colab
2. Mount your Google Drive and adjust the file paths accordingly:
```python
from google.colab import drive
drive.mount('/content/drive')
```
3. Update the dataset paths in the notebook to point to your uploaded datasets

### Expected Outputs

After running the notebook, you can get the expected results.

## Technologies Used

All implementations are written in Python and are flexible enough to be extended to other datasets with minor changes. The code can be executed in Jupyter Notebook or Google Colab with minimal modifications.

## Research Significance

This research contributes to the field of transfer learning and domain adaptation by providing methods to extract information from image datasets and establish similarities between different datasets. The implemented techniques (Grad-CAM, AAD, Optimal Transport, Direct Domain Adaptation) can be applied to solve real-life problems where specialized data is limited.

## Acknowledgements

I would like to express my sincere gratitude to:

- **Prof. Dr. C. Krishna Mohan, IIT Hyderabad** - For their invaluable guidance, support, and mentorship throughout the internship
- **VIGIL Lab, IIT Hyderabad** - For providing the opportunity and resources to conduct this research
- **Dr. Udaya Kumar Ambati** - For their collaborative efforts and insightful discussions
- **Kaggle and Dataset Contributors** - For making the datasets publicly available for research
- **Research Communities** - For the foundational work in Grad-CAM, AAD, and domain adaptation techniques that made this research possible
