# Multi_Class_Animal_Classification
## Week 1: Data Exploration and Visualization

**Objective:** Understand the dataset and prepare it for model training.

### ✅ Tasks Completed:

- Implemented code to **randomly display sample images** from 10 animal classes
- **Filtered valid image formats** to prevent processing errors
- **Resized all images** to a consistent 224×224 resolution for better display
- **Counted the number of images per class** to detect potential class imbalance
- Improved **readability, consistency and robustness** of dataset loading code

➡ [Click here to view the Week 1 Notebook](week1.ipynb)

## 📅 Week 2: Data Preprocessing & Augmentation

**Objective:** Prepare the dataset using Keras' `ImageDataGenerator` for MobileNetV2 model training.

### ✅ Summary of Work:

- Defined image size (224×224) and batch size (64) suitable for MobileNetV2
- Applied image rescaling (`1./255`) and split data into training (90%) and validation (10%) sets
- Created train and validation generators using `flow_from_directory`
- Added a `seed` for reproducible data splits
- Filtered out unsupported or corrupted images to avoid errors
- Printed the number of images in each split to verify dataset balance
- Extracted and sorted class labels alphabetically for better readability
- Structured code with clear comments and logical sections for improved clarity

➡️ [View Week 2 Notebook](week2/week2_task.ipynb)

