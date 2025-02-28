# nail-agastya-munjal-repo
Portable Nail Infection Detection System Using Advanced Image Processing Techniques <br>
*Author* : AGASTYA MUNJAL

This project develops an embedded vision system for non-invasive detection of nail infections, distinguishing between **Onychomycosis** and **Healthy Nail** classes. It integrates spectral imaging with deep learning algorithms, specifically lightweight Convolutional Neural Networks (CNNs), for edge deployment. The system aims to address limitations in traditional diagnostics (e.g., KOH preparation, fungal cultures) by providing rapid, accurate classification using hybrid feature extraction and multi-spectral imaging.

### Research Objectives
- **Multi-spectral Imaging**: Capture nail plate images under variable lighting conditions.
- **Automated Segmentation**: Isolate regions like the lunula and hyponychium.
- **Hybrid Feature Extraction**: Combine textural and chromatic features for robust classification.
- **Edge Deployment**: Optimize for lightweight, portable devices.

### Workflow
1. **Examine and preprocess nail image data**: Analyze the dataset to understand image characteristics, count samples per class (Onychomycosis and Healthy Nail), and preprocess images by resizing, normalizing, and applying multi-spectral transformations to enhance chromatic details critical for infection detection.
2. **Build an input pipeline with augmentation and spectral processing**: Create a data pipeline using augmentation (rotation, flip) to increase robustness and incorporate spectral preprocessing (e.g., HSV stacking) to simulate multi-spectral imaging, ensuring the model handles variable lighting conditions effectively.
3. **Develop a lightweight CNN model**: Design a compact CNN with convolutional layers for hybrid feature extraction (texture and color) and dropout for regularization, optimized for low computational overhead suitable for edge devices while maintaining diagnostic accuracy.
4. **Train and evaluate the model**: Train the CNN on the preprocessed dataset, monitor performance metrics (accuracy, loss) over epochs, and evaluate generalization on a validation set to ensure reliable classification of nail infections.
5. **Test with static images and real-time webcam input**: Validate the model on static nail images via a user interface and enable real-time detection using webcam feeds, integrating segmentation and spectral preprocessing for practical diagnostic deployment.
6. **Convert to TensorFlow Lite for edge deployment**: Convert the trained model to TensorFlow Lite format, optimizing it for portable devices, ensuring low latency and resource efficiency for non-invasive nail infection screening in real-world settings.
