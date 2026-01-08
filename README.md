# Hairstyle Recommendation System - Deployment Package

## Contents

### Models Directory
- svm_face_shape_classifier.pkl - SVM model for face shape classification
- mlp_hairstyle_recommender.h5 - MLP model for hairstyle recommendation
- preprocessing_objects.pkl - Preprocessing objects for SVM
- mlp_preprocessing_objects.pkl - Preprocessing objects for MLP
- shape_predictor_68_face_landmarks.dat - dlib facial landmark detector

### Data Directory
- male_faces_with_shapes.csv - Training dataset with face shape labels
- hairstyle_dataset.csv - Complete dataset with hairstyle recommendations
- male_face_features.csv - Extracted geometric features

### Documentation Directory
- Performance reports and visualizations

## Model Performance
- Face shape detection: 95.57% accuracy
- Hairstyle recommendation: 98.09% accuracy
