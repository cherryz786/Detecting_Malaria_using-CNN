# Malaria Detection using CNN

## Overview

This project aims to facilitate faster and efficient detection of malaria through the use of Convolutional Neural Networks (CNNs). By leveraging a dataset consisting of 27,558 images sourced from the NIH Website [Malaria Datasets](https://ceb.nlm.nih.gov/repositories/malaria-datasets/), we have developed a model that enhances the diagnostic capabilities for detecting infected and uninfected cells.

## Benefits

- **Faster Detection**: The CNN model is designed to rapidly analyze and classify images, providing quick results for malaria detection.
- **Efficiency Maximization for Doctors**: By automating the detection process, doctors can optimize their efficiency, allowing for better allocation of time and resources towards treatment.

## Dataset

The dataset comprises two folders: Infected and Uninfected, with a total of 27,558 images.

## Libraries Used

```python
import os
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from matplotlib.image import imread
from tensorflow.keras.preprocessing.image import ImageDataGenerator
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Activation, Dropout, Flatten, Dense, Conv2D, MaxPooling2D
