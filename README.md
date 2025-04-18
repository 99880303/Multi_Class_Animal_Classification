# 🐾 Multi-Class Animal Recognition for Wildlife Conservation

This project focuses on developing a deep learning model capable of classifying images of 90 different animal species. Leveraging transfer learning with MobileNetV2, the model supports wildlife conservation efforts by providing an efficient, scalable, and accurate system to identify animals in images.

---

## 🎯 Objective

- Build a robust image classification system for 90 animal species.
- Automate species identification to support conservation and wildlife monitoring.
- Reduce manual efforts in categorizing wildlife data.

---

## 🛠️ Tools & Technologies Used

- **Languages & Libraries:** Python, TensorFlow, Keras, NumPy, Matplotlib
- **Model:** MobileNetV2 (Transfer Learning)
- **Development Environment:** Jupyter Notebook
- **Dataset:** [Animal Image Dataset (90 Classes)](https://www.kaggle.com/datasets/alessiocorrado99/animals10)

---

## 🔍 Methodology

- **Dataset Preparation:** Organized dataset and visualized random images with consistent shape (224x224).
- **Preprocessing:** Used `ImageDataGenerator` for normalization and augmentation, with training/validation split.
- **Modeling:** Loaded pre-trained MobileNetV2, froze base layers, and added custom dense layers.
- **Training:** Trained the model for 20 epochs using Adam optimizer with categorical crossentropy loss.
- **Evaluation:** Visualized training/validation accuracy and loss; evaluated final model performance.
- **Prediction:** Created a reusable function to predict and visualize the class of new images.

---

## ✅ Key Features & Improvements

- Filtered valid image formats to avoid loading errors and improve dataset reliability.
- Ensured all images are resized consistently for better training performance.
- Computed and printed class-wise image counts to check for class imbalance.
- Optimized preprocessing and augmentation techniques to improve model generalization.
- Built a modular prediction function to test model on unseen data.
- Visualized training metrics using clean and labeled plots.
- Maintained clean, readable, and scalable code for future extensions.

---

## 📈 Results

- ✅ Achieved ~85% validation accuracy on a 90-class classification task.
- 🔍 Successfully predicted unseen images using the trained model.
- 📉 Clear learning curves indicating good training/validation performance.

---

## 🖼️ Sample Prediction Function

```python
def predict_animal(img_path):
    img = image.load_img(img_path, target_size=(224, 224))
    img_array = image.img_to_array(img)
    img_array = np.expand_dims(img_array, axis=0) / 255.0

    prediction = model.predict(img_array)
    predicted_class = class_names[np.argmax(prediction)]

    plt.imshow(img)
    plt.title(f"Predicted: {predicted_class}")
    plt.axis('off')
    plt.show()


