# ImageClassificationModel-catVdog-
# Image Classification Model Using Convolutional Neural Networks (CNN)

## Author
**Suniya Firdous Khan**  
3rd Year, 5th Semester  
Department of Artificial Intelligence & Data Science  

## Project Overview
This project aims to develop an image classification model that can differentiate between two classes—dogs and cats—using Convolutional Neural Networks (CNN). The model is trained on a dataset of dog and cat images, focusing on achieving accurate classification for new, unseen images.

## Objective
The objective of this project is to:
- Develop an image classification model using CNN.
- Achieve high accuracy in classifying images of dogs and cats.

## Dataset
- **Training Set:** 20,000 images belonging to 2 classes (dogs and cats).
- **Validation Set:** 5,000 images belonging to 2 classes.

### Dataset Source
The dataset can be found on [Kaggle](https://www.kaggle.com/datasets/salader/dogs-vs-cats).

## Data Preprocessing
Several preprocessing steps were performed before feeding the data into the model:
1. **Rescaling:** The pixel values were normalized to a range of 0 to 1.
2. **Resizing:** All images were resized to 256x256 pixels.
3. **Batch Processing:** Data was loaded in batches of 32 for efficient handling.
4. **Label Inference:** Labels were inferred from the directory structure (0 for cats, 1 for dogs).

## CNN Model Architecture
The CNN model was implemented using Keras with the following structure:
- **Input Layer:** Image input of size (256, 256, 3).
- **Convolutional Layers:** 
  - Conv2D Layer 1
  - Conv2D Layer 2
  - Conv2D Layer 3
- **Flatten Layer:** Flattened to a 1D vector.
- **Dense Layers:** 
  - Dense Layer 1: 128 units with ReLU activation, followed by Dropout (0.1).
  - Dense Layer 2: 64 units with ReLU activation, followed by Dropout (0.1).
- **Output Layer:** A single neuron with sigmoid activation.

### Model Summary
- **Total Parameters:** 14,848,193
- **Trainable Parameters:** 14,847,745

## Training the Model
The model was trained for 10 epochs with a batch size of 32. The validation dataset was used to evaluate the performance after each epoch.

### Training Results
- **Final Training Accuracy:** 96.43%
- **Final Validation Accuracy:** 82.06%
- **Final Training Loss:** 0.0982
- **Final Validation Loss:** 0.5862

## Testing the Model
The trained model was tested on two images:
1. **Dog Image:** Correctly classified with a predicted output of 1 (dog).
2. **Cat Image:** Correctly classified with a predicted output of 0 (cat).

## Visualization
Key performance metrics were visualized:
- **Training vs Validation Accuracy:** Training accuracy improved while validation accuracy fluctuated around 82%.
- **Training vs Validation Loss:** Training loss decreased, but validation loss fluctuated, indicating potential overfitting.

## Conclusion
The CNN model successfully classified images of dogs and cats with a validation accuracy of 82% after 10 epochs. Further improvements could be achieved using techniques like data augmentation to mitigate overfitting.

## License
This project is licensed under the [MIT License](LICENSE).
