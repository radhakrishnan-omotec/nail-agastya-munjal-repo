# nail-agastya-munjal-repo
Portable Nail Infection Detection System Using Advanced Image Processing Techniques <br>
*Author* : AGASTYA MUNJAL

This project develops an embedded vision system for non-invasive detection of nail infections, distinguishing between **Onychomycosis** and **Healthy Nail** classes. It integrates spectral imaging with deep learning algorithms, specifically lightweight Convolutional Neural Networks (CNNs), for edge deployment. The system aims to address limitations in traditional diagnostics (e.g., KOH preparation, fungal cultures) by providing rapid, accurate classification using hybrid feature extraction and multi-spectral imaging.

---

### Research Objectives
- **Multi-spectral Imaging**: Capture nail plate images under variable lighting conditions.
- **Automated Segmentation**: Isolate regions like the lunula and hyponychium.
- **Hybrid Feature Extraction**: Combine textural and chromatic features for robust classification.
- **Edge Deployment**: Optimize for lightweight, portable devices.

---

### Workflow
1. **Examine and preprocess nail image data**: Analyze the dataset to understand image characteristics, count samples per class (Onychomycosis and Healthy Nail), and preprocess images by resizing, normalizing, and applying multi-spectral transformations to enhance chromatic details critical for infection detection.
2. **Build an input pipeline with augmentation and spectral processing**: Create a data pipeline using augmentation (rotation, flip) to increase robustness and incorporate spectral preprocessing (e.g., HSV stacking) to simulate multi-spectral imaging, ensuring the model handles variable lighting conditions effectively.
3. **Develop a lightweight CNN model**: Design a compact CNN with convolutional layers for hybrid feature extraction (texture and color) and dropout for regularization, optimized for low computational overhead suitable for edge devices while maintaining diagnostic accuracy.
4. **Train and evaluate the model**: Train the CNN on the preprocessed dataset, monitor performance metrics (accuracy, loss) over epochs, and evaluate generalization on a validation set to ensure reliable classification of nail infections.
5. **Test with static images and real-time webcam input**: Validate the model on static nail images via a user interface and enable real-time detection using webcam feeds, integrating segmentation and spectral preprocessing for practical diagnostic deployment.
6. **Convert to TensorFlow Lite for RPI edge deployment**: Convert the trained model to TensorFlow Lite format, optimizing it for portable devices, ensuring low latency and resource efficiency for non-invasive nail infection screening in real-world settings.





### Step 1: Examine and Preprocess Nail Image Data
This step involves loading and analyzing the nail image dataset to assess its size and class distribution (Onychomycosis vs. Healthy Nail). With 18-23% of the global population affected by nail disorders, understanding data composition is key. Images are preprocessed by resizing to 180x180, normalizing pixel values, and applying multi-spectral transformations (e.g., HSV conversion) to enhance chromatic features critical for detecting infection markers like discoloration or texture changes. This ensures the dataset is ready for robust model training, addressing the research goal of multi-spectral nail bed imaging.



### Step 2: Build an Input Pipeline with Augmentation and Spectral Processing
An input pipeline is constructed to feed images into the model efficiently. Data augmentation (rotation, flipping, zoom) increases dataset diversity, mitigating overfitting and simulating real-world variability. Spectral processing, using HSV channel stacking, mimics multi-spectral imaging to capture nail bed color variations under different lighting conditions, a key research challenge. Segmentation isolates nail regions (e.g., lunula), enhancing focus on infection-relevant areas. This pipeline ensures the model learns robust features, aligning with the goal of automated segmentation and multi-spectral analysis for accurate diagnostics.



### Step 3: Develop a Lightweight CNN Model
A lightweight CNN is designed for edge deployment, featuring fewer layers and parameters to minimize computational load while retaining diagnostic accuracy. Convolutional layers extract hybrid features—textural (e.g., nail surface irregularities) and chromatic (e.g., discoloration)—critical for distinguishing Onychomycosis from Healthy Nails. Dropout layers (0.25, 0.5) reduce overfitting, ensuring generalization. This architecture supports the research goal of hybrid feature extraction and is optimized for portable devices, addressing the need for a rapid, non-invasive screening tool deployable in resource-constrained environments.



### Step 4: Train and Evaluate the Model
The CNN is trained over 20 epochs using the preprocessed dataset, optimizing for binary cross-entropy loss and accuracy. Training progress is monitored via accuracy and loss metrics, with a validation set assessing generalization to unseen data. This step ensures the model learns to differentiate Onychomycosis from Healthy Nails reliably, overcoming limitations of traditional methods (e.g., 58-67% sensitivity of KOH tests). Evaluation plots provide insights into overfitting, guiding adjustments to improve performance, aligning with the research aim of accurate, automated diagnostics.



### Step 5: Test with Static Images and Real-Time Webcam Input
The trained model is tested on static images via a Gradio UI, allowing users to upload nail photos for classification, and on real-time webcam feeds for live detection. Both methods apply segmentation and spectral preprocessing, ensuring practical applicability. This step validates the system’s non-invasive diagnostic capability, addressing the research challenge of real-world deployment. The webcam integration simulates clinical use, providing instant feedback on nail health, making it a viable alternative to slow fungal cultures (45-60 day latency).



### Step 6: Convert to TensorFlow Lite for RPI Edge Deployment
The trained CNN is converted to TensorFlow Lite, a lightweight format optimized for edge devices like portable imaging systems. This step reduces model size and inference time, ensuring low latency and minimal resource use—crucial for deploying the system in clinics or homes. By enabling on-device processing, it supports the research vision of a standalone, non-invasive diagnostic tool, replacing cumbersome traditional methods with a rapid, efficient solution for nail infection screening.
