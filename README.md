# Netflix Content Recommendation System

Developed a deep learning–based content recommendation system using a Netflix 2023 dataset. 
The goal was to recommend similar movies or shows based on metadata such as language, content type, and viewing hours. 
Performed data preprocessing and feature encoding using Pandas, then built a neural recommendation model with embedding layers using TensorFlow/Keras. 
The trained model learns relationships between content items and generates recommendations by identifying similar titles in the learned embedding space.


## Tools and Technologies Used
The following tools and libraries were used to build the system:

- **Python** for implementation
- **Pandas** for data cleaning and preprocessing
- **NumPy** for numerical operations
- **TensorFlow / Keras** for building the neural network model
- **Embeddings** for learning relationships between categorical features

## Approach and Solution

### Data Preprocessing
The Netflix dataset contained information such as titles, language, content type, and hours viewed. The preprocessing steps included:

- Cleaning the `Hours Viewed` column by removing commas and converting it to numeric format
- Removing rows with missing titles
- Removing duplicate titles
- Encoding categorical features such as language and content type into numerical IDs
- Creating a unique `Content_ID` for each title

These transformations allowed the data to be used as input for a neural network model.

### Model Design
A neural recommendation model was built using TensorFlow. The model uses **embedding layers** to convert categorical features (content ID, language, and content type) into dense numerical vectors. These embeddings allow the model to learn similarity relationships between content items.

The embeddings are combined and passed through dense neural network layers to predict similar content.

### Training
The model was trained using a **self-supervised learning approach**, where the system learns to predict content items based on their metadata features. During training, the embeddings learn patterns that group similar content closer together in the feature space.

### Generating Recommendations
After training, the system can take a content title as input and generate recommendations by predicting similar content IDs. The model identifies the closest items in the learned embedding space and returns the corresponding titles from the dataset.

## Result
The final system can recommend similar movies or shows based on content metadata such as language, type, and viewing patterns. This demonstrates how deep learning and embeddings can be used to build recommendation systems even without explicit user interaction data.
