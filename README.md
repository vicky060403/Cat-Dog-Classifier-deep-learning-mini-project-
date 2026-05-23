# 🐱 Dog vs Cat Classifier 🐶

A simple yet powerful image classification application that can distinguish between dogs and cats using a Convolutional Neural Network (CNN) built with TensorFlow/Keras.

## 📈 Model Performance

The CNN model was trained and optimized using BatchNormalization, data augmentation and hyperparameter tuning.

### Results

- **Training Accuracy:** 79.69%
- **Validation Accuracy:** 74.37%
- **Validation Loss:** 0.5507

These results indicate that the model learned useful patterns while maintaining reasonable generalization on unseen validation data.

## ✨ Features

- 🖼️ Upload and classify images of dogs and cats
- 📊 View prediction confidence with visual indicators
- 🧠 Trained CNN model with good accuracy
- 🖥️ Streamlit web interface for easy interaction
- 📝 Command-line interface for inferencing

## 🛠️ Installation

### Prerequisites

- Python 3.10+ installed
- pip package manager

### Option 1: Standard Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/vicky060403/Cat-Dog-Classifier-deep-learning-mini-project-.git
   cd Dog-Cat-Classifier-deep-learning-mini-project-
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

### Web Interface

Run the Streamlit app:
```bash
streamlit run streamlit_app.py
```

Then open your browser and navigate to the URL shown in the terminal (typically http://localhost:8501).

### Command Line Interface

For quick predictions without the web interface:
```bash
python cli.py path/to/your/image.jpg
```

Optional arguments:
- `--model`: Specify a different model file (default: dog_cat_cnn_model.h5)

Example:
```bash
python cli.py samples/my_cat.jpg --model models/custom_model.h5
```

## 🧪 Model Training

The model was trained on a dataset of dog and cat images. The training process is documented in `training_a_cnn_with_custom_dataset_keras.py`.

Key model architecture:
- Input: 128×128 RGB images
- 3 Convolutional layers with MaxPooling
- BatchNormalization for stable training
- Dropout layers for regularization
- ModelCheckpoint callbacks
- Binary classification output using Sigmoid activation

## 📁 Project Structure

```text
Cat-Dog-Classifier-deep-learning-mini-project/
├── data/                                  # Training and validation images
├── dataset/                               # Dataset folder
├── Training_a_CNN_with_Custom_Dataset_Keras.ipynb
│                                           # Model training notebook
├── streamlit_app.py                       # Streamlit web interface
├── webapp.py                              # Web application logic
├── main.py                                # Main execution file
├── cli.py                                 # Command line interface
├── dog_cat_cnn_model.keras                # Saved CNN model
├── dog_cat_final_model.keras              # Final trained model
├── requirements.txt                       # Dependencies
└── README.md                              # Project documentation
```

## Improvements Made

- Added BatchNormalization to improve training stability
- Added ModelCheckpoint to save best-performing model
- Enhanced image augmentation strategy
- Fixed validation pipeline issues
- Tuned optimizer and learning rate
- Improved validation performance and generalization

## Future Improvements

- Try transfer learning (MobileNetV2 / ResNet)
- Add real-time image upload

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- Dataset from Kaggle's Dogs vs Cats competition
- Built with TensorFlow and Streamlit