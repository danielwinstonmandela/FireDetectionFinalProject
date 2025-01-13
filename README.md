# Fire Detection in Digital Images  
**Using Enhanced Image Processing and Machine Learning Techniques**

### Table of Contents
1. [Introduction](#introduction)  
2. [Objective](#objective)  
3. [Methodology](#methodology)  
   - [Data Acquisition](#data-acquisition)  
   - [Image Enhancement](#image-enhancement)  
   - [Segmentation](#segmentation)  
   - [Feature Extraction](#feature-extraction)  
   - [Classification](#classification)  
4. [Results](#results)  
5. [Repository Contents](#repository-contents)  
6. [Contributors](#contributors)

---

### Introduction
Fires can start quickly in both enclosed and open environments, making early and accurate fire detection crucial to minimize damage and save lives. This project develops a robust system using digital image processing and machine learning techniques to detect fire with high accuracy.

---

### Objective
To create a reliable fire detection system that identifies fire occurrences while minimizing false positives, ensuring efficient and focused responses to genuine threats.

---

### Methodology

#### Data Acquisition
- Dataset: 760 fire and 760 non-fire images from Kaggle.  
- Images represent various lighting and weather conditions for real-world applicability.

#### Image Enhancement
- **Color Space Conversion**: HSV channel separation for isolating fire-like colors.  
- **Contrast Stretching**: Enhances brightness for consistent quality.  

#### Segmentation
1. **Color Segmentation**: Isolates fire-like regions using HSV thresholds.  
2. **Otsu’s Thresholding**: Reduces false positives caused by non-fire objects.  
3. **Sobel Edge Detection**: Identifies boundaries of fire regions.  
4. **Morphological Operations**: Smoothens regions and removes noise.  
5. **Contour Detection**: Focuses on primary fire areas for tracking.

#### Feature Extraction
- **Geometric Features**: Area, perimeter, aspect ratio.  
- **Color Features**: Mean HSV values.  
- **Texture Features**: Extracted using Local Binary Patterns (LBP).  
- **Gradient Features**: Captures intensity changes.

#### Classification
- **Support Vector Machine (SVM)**:  
   - **Training Phase**: Learns patterns from extracted features.  
   - **Testing Phase**: Classifies new images as "fire" or "non-fire."

---

### Results

The performance of the fire detection system was evaluated using precision, recall, F1-score, and accuracy metrics. Below are the detailed results:

| Class           | Precision | Recall | F1-Score | Support |
|------------------|-----------|--------|----------|---------|
| 0 (Non-Fire)    | 0.84      | 0.97   | 0.90     | 147     |
| 1 (Fire)        | 0.97      | 0.80   | 0.88     | 157     |
| **Accuracy**    | -         | -      | **0.89** | 304     |
| **Macro Average** | 0.90    | 0.89   | 0.89     | 304     |
| **Weighted Average** | 0.90 | 0.89   | 0.89     | 304     |

#### Summary
- The model achieved an overall accuracy of **89%**, demonstrating its effectiveness in distinguishing between fire and non-fire images.
- The precision for detecting fire images (class 1) is notably high at **97%**, ensuring minimal false positives.
- Recall for fire detection is **80%**, indicating that some fire cases might be missed, which could be improved with more diverse training data.
- The F1-score of **0.88** for fire detection reflects a balanced trade-off between precision and recall.

#### Visualization
- The confusion matrix and visualized predictions can be found in the Jupyter Notebook (`fire_detection.ipynb`).  
- **Fig. 4** in the IEEE report provides a detailed graphical representation of the fire detection results.


![image](https://github.com/user-attachments/assets/22163b83-7198-4ab4-8b5a-bb99cdbc0453)

---

### Repository Contents
- **`fire_detection.ipynb`**: Jupyter Notebook containing the implementation of the fire detection model.  
- **`IEEE_Report.pdf`**: Technical report in IEEE format detailing the methodology and results.  
- **`Presentation_Deck.pdf`**: Slide deck summarizing the project.  


---

### Contributors
- **Daniel Winston Mandela Tulung** 
- **Girindra Daafi Mada**  
- **Keefani Mentari Ingprairie** 
- **Naura Ayesha Tsaqif**  
