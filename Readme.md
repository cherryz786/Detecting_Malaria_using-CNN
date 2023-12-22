# Malaria Detection using CNN

## Overview

This project employs Convolutional Neural Networks (CNNs) for rapid and efficient malaria detection. Using a dataset of 27,558 images from the [NIH Malaria Datasets](https://ceb.nlm.nih.gov/repositories/malaria-datasets/), the model enhances diagnostic capabilities for identifying infected and uninfected cells.

## Benefits

- **Faster Detection**: Quickly analyzes and classifies images for swift malaria detection.
- **Efficiency for Doctors**: Automates the detection process, optimizing doctors' efficiency for better resource allocation.

## Dataset

- 27,558 images in two folders: Infected and Uninfected.

## Libraries Used

- `os`
- `pandas`
- `numpy`
- `seaborn`
- `matplotlib.pyplot`
- `tensorflow.keras.preprocessing.image.ImageDataGenerator`
- `tensorflow.keras.models.Sequential`
- `tensorflow.keras.layers`

## Data Augmentation

- Utilized `ImageDataGenerator` for image manipulation.

## CNN Model Architecture

- Three sets of Convolution and Pooling layers.

```python
model = Sequential()
# ... Convolution and Pooling Layers ...
model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])
```

## Early Stopping
Implemented using the EarlyStopping callback.
```python
early_stop = EarlyStopping(monitor='val_loss', patience=2)
```

## Training
Batch size: 16
Classification report:
```yaml
Copy code
precision    recall  f1-score   support
0       0.97      0.93      0.95      1300
1       0.94      0.97      0.95      1300
accuracy                           0.95      2600
```
