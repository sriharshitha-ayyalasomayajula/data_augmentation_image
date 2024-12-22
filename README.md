# Data Augmentation for Vehicle Detection with Generative AI

This project explores advanced image data augmentation techniques to enhance and diversify training datasets for vehicle detection tasks. The dataset used is the [Top-View Vehicle Detection Dataset](https://www.kaggle.com/datasets/farzadnekouei/top-view-vehicle-detection-image-dataset). The project integrates cutting-edge generative AI models and traditional augmentation methods to improve the performance of object detection models like YOLOv8.

## Project Overview

### Objective
To enhance vehicle detection accuracy by expanding the dataset with augmented and synthetic images.

### Dataset
- **Source**: Kaggle's Top-View Vehicle Detection Dataset
- **Composition**: 
  - 400 training images and labels
  - 33 validation images and labels

### Augmentation Techniques
1. **Geometric Augmentation**:
   - Utilizes Keras' `ImageDataGenerator` for random rotations, flips, zooms, etc.
   - Generates 5 augmented samples per input image.

2. **BigGAN Model**:
   - Produces synthetic images of vehicles using a pre-trained BigGAN model.
   - Generates 1 synthetic sample per input image.

3. **Stable Diffusion Model**:
   - Creates descriptive prompts to generate new images.
   - Produces 1 new sample per input image using a pre-trained Stable Diffusion model.

### Applications
- Augmented images are uploaded to a Google Cloud Storage (GCS) bucket for use in future training or evaluation.
- Inference is performed using a pre-trained YOLOv8 model to evaluate the effectiveness of augmented data.


## Implementation Details

### Data Loading
- Define storage client variables to access data from Google Cloud Storage (GCS).
- Load the datasets into appropriate local directories.

### Augmentation Techniques
1. Apply geometric transformations using Keras.
2. Generate synthetic images using BigGAN and Stable Diffusion.

### Inference
- Perform vehicle detection using YOLOv8 on the augmented dataset.

---

## Files in the Repository

- **`Data_Augmentation_Image.ipynb`**: Main notebook for implementing data augmentation and vehicle detection.
- **`Requirements.txt`**: List of dependencies required for the project.

---

## Conclusion

This project demonstrates how **Generative AI** and **data augmentation techniques** can enhance datasets for object detection tasks, leading to better model performance. The integration of traditional and generative augmentation methods showcases a scalable approach for improving model accuracy in real-world applications.

