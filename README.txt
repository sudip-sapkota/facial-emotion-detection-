# Facial Emotion Detection Project - Complete Setup Guide

## Project Overview
This project implements a deep learning system for facial emotion recognition specifically designed for people wearing face masks. The model classifies 7 emotions (angry, disgust, fear, happy, neutral, sad, surprise) and includes comprehensive bias analysis across demographic groups.

## Prerequisites
1. Python 3.8 or higher
2. Jupyter Notebook or JupyterLab
3. Internet connection for downloading datasets

## Installation Instructions

### Step 1: Install Required Libraries
Run this command in your terminal/command prompt:
```
pip install -r requirements.txt
```

### Step 2: Download and Setup Datasets

#### 2.1 Download the CSV Dataset
1. Go to this Google Drive link:
   https://drive.google.com/file/d/1CLYsOFXxsufaIH0BKoS39iOuvckM1rwn/view?usp=drive_link

2. Click "Download" button
3. Save the file as "facial_emotion_dataset_with_metadata.csv" in the project root directory

#### 2.2 Download the Archive Dataset
1. Go to this Google Drive link:
   https://drive.google.com/drive/folders/1HBIMIl3X2hoCmJ7VgO7lbP0SyemVuFzC?usp=drive_link

2. Download the entire "archive" folder 
3. Extract it to the project root directory (same folder as this README.txt)
4. The folder structure should look like:
   ```
   Facial_Emotion_Detection_Assignment2/
   ├── README.txt (this file)
   ├── facial_emotion_detection_project.ipynb
   ├── facial_emotion_dataset_with_metadata.csv
   ├── archive/
   │   └── masked_dataset/
   │       ├── test/
   │       └── train/
   ├── requirements.txt
   └── other project files...
   ```

### Step 3: Verify File Structure
Before running the project, make sure you have these files in your directory:
- facial_emotion_detection_project.ipynb
- facial_emotion_dataset_with_metadata.csv
- archive/masked_dataset/ folder

## Running the Project

### Option 1: Using Jupyter Notebook
1. Open terminal/command prompt in the project directory
2. Run: `jupyter notebook`
3. Open "facial_emotion_detection_project.ipynb"
4. Run all cells sequentially (Cell → Run All)

### Option 2: Using JupyterLab
1. Open terminal/command prompt in the project directory
2. Run: `jupyter lab`
3. Open "facial_emotion_detection_project.ipynb"
4. Run all cells sequentially

### Option 3: Using Google Colab
1. Upload the notebook file to Google Colab
2. Upload the datasets to your Colab environment
3. Modify the file paths in the notebook if needed
4. Run all cells

## Dataset Information

### CSV Dataset (facial_emotion_dataset_with_metadata.csv)
- Contains 20,484 samples
- 6 columns: split, emotion, age, gender, ethnicity, pixels
- Emotions: angry, disgust, fear, happy, neutral, sad, surprise
- Pixel values represent 48x48 grayscale images

### Image Dataset (archive/masked_dataset/)
- Contains actual image files organized by emotion
- Images of people wearing face masks
- Used for training and testing the deep learning model

## Troubleshooting

### Problem: Charts not displaying
If you're not seeing charts in your notebook:
1. Make sure matplotlib is installed: `pip install matplotlib`
2. Add this magic command at the beginning of your notebook:
   ```python
   %matplotlib inline
   ```
3. Restart the kernel and run all cells again

### Problem: Dataset not found
1. Check file paths in the notebook:
   - csv_path = "facial_emotion_dataset_with_metadata.csv"
   - image_path = "archive/masked_dataset"
2. Ensure files are in the correct location
3. Check file names match exactly (case-sensitive)

### Problem: Model training errors
1. Ensure all dependencies are installed
2. Check if you have enough RAM (recommended: 8GB+)
3. Try reducing batch size if memory issues occur

### Problem: CUDA/GPU errors
If you encounter GPU-related errors:
1. The project will automatically fall back to CPU
2. Training will be slower but still functional
3. Consider using Google Colab for free GPU access

## Project Features

1. **Data Analysis**: Comprehensive exploration of the emotion dataset
2. **Preprocessing**: Image normalization and data augmentation
3. **Model Architecture**: CNN with transfer learning (VGG16 base)
4. **Training**: With early stopping and learning rate scheduling
5. **Evaluation**: Detailed metrics, confusion matrix, and bias analysis
6. **Visualization**: Charts showing emotion distribution and model performance

## Expected Outputs

When running successfully, you should see:
1. Dataset loading confirmation
2. Emotion distribution charts
3. Sample image visualizations
4. Model training progress
5. Performance metrics and accuracy scores
6. Confusion matrix visualization
7. Bias analysis across demographic groups

## Additional Notes

- The project includes pre-trained models (FINAL_SUBMISSION_MODEL.h5, best_model.h5)
- Training typically takes 30-60 minutes depending on your hardware
- All random seeds are set for reproducible results
- The model achieves approximately 85-90% accuracy on the test set

## Support

If you encounter any issues:
1. Check that all files are in the correct locations
2. Verify all required libraries are installed
3. Ensure you have sufficient system resources
4. Check the notebook output for specific error messages

For questions about the implementation, refer to the detailed comments in the notebook cells.

## License

This project is for educational purposes. Please respect the original dataset licenses and terms of use.

---
Last updated: September 2025
