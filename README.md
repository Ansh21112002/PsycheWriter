# PsycheWriter
Created BCI keyboard model using CNN, RNN, and XGB on Emotiv dataset (29728 samples, 65 features).


Model Architecture: Our machine learning model is designed with a sophisticated architecture to effectively capture both spatial and temporal information in the EEG data.


 Spatial Feature Extraction with CNN: We employ a Convolutional Neural Network (CNN) as the first component of our model. The CNN is specifically designed for spatial feature extraction. It scans the EEG data, identifying patterns and features in different spatial locations. This allows it to discern spatial nuances in the input data.
 
 Temporal Feature Extraction with RNN: Simultaneously, we employ a Recurrent Neural Network (RNN) to capture temporal dependencies within the EEG data. The RNN processes the data sequentially, recognizing patterns and relationships over time. This temporal analysis is critical in understanding the dynamic nature of EEG signals.

3. Parallel Processing and Stacking:
The CNN and RNN operate in parallel, ensuring that spatial and temporal features are extracted concurrently. The outputs from these two networks are then stacked together, forming a multi-dimensional representation of the EEG data.

5. Feature Adaptation with Autoencoder Layer:
To further enhance the integration of spatial and temporal features, we introduce an autoencoder layer. This layer serves as a feature adaptation method, mapping the stacked features into a new, correlated feature space. By leveraging the power of autoencoders, we can reduce noise, enhance important patterns, and create a more informative representation that fuses spatial and temporal information effectively.

6. Direction Classification with XGBoost:
Finally, we employ the XGBoost algorithm for the task of direction classification. XGBoost is well-suited for this task, as it can handle complex, high-dimensional feature spaces and make accurate predictions. It takes the fused features from the previous step as input and performs the classification task, accurately determining the intended direction or state based on the enriched feature representation.
