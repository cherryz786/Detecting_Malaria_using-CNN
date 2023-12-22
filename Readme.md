# Malaria Detection in blood cells

![Untitled design (2)](https://github.com/cherryz786/Detecting_Malaria_using-CNN/assets/71602299/9839adc4-b32d-462c-8cd5-621024295382)
(using CNN)

## Overview

This project employs Convolutional Neural Networks (CNNs) for rapid and efficient malaria detectionin bood cells. Using a dataset of 27,558 images from the [NIH Malaria Datasets](https://ceb.nlm.nih.gov/repositories/malaria-datasets/), the model enhances diagnostic capabilities for identifying infected and uninfected cells.

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

- To address the challenge of limited images, we employed image manipulation techniques using the `ImageDataGenerator` from TensorFlow:
```python
image_gen = ImageDataGenerator(
    rotation_range=20,
    width_shift_range=0.10,
    height_shift_range=0.10,
    rescale=1/255,
    shear_range=0.1,
    zoom_range=0.1,
    horizontal_flip=True,
    fill_mode='nearest'
)
```

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
- Batch size: 16
- Classification report:
```yaml
Copy code
precision    recall  f1-score   support
1.  0.97      0.93      0.95      1300
2.  0.94      0.97      0.95      1300
accuracy: 0.95
```
