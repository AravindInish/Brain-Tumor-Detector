<div align="center">

🧠 Brain Tumor Detection Using Deep Learning

An MRI Image Classification Web App Powered by CNN & Streamlit

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white" alt="Keras">
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
</p>

<p>
  <img src="https://img.shields.io/badge/Computer%20Vision-Image%20Classification-6A5ACD?style=flat-square" alt="Computer Vision">
  <img src="https://img.shields.io/badge/Deep%20Learning-CNN-0A7EA4?style=flat-square" alt="Deep Learning">
  <img src="https://img.shields.io/badge/Status-Educational%20Project-success?style=flat-square" alt="Project Status">
</p>

Upload a brain MRI image and get a model-generated prediction for the presence or absence of a tumor.

✨ Features · 🛠️ Tech Stack · ⚙️ Installation · 🚀 Run the App · ⚠️ Disclaimer

</div>

📌 About the Project

Brain Tumor Detection is a deep-learning project that uses a Convolutional Neural Network (CNN) to classify brain MRI images into two categories:

🟢 No Tumor Detected

🔴 Tumor Detected

The project includes a Streamlit web interface where users can upload an MRI image, preview it, and view the model's predicted class alongside a confidence score.

🎯 Project goal: Demonstrate an end-to-end computer vision workflow—from dataset preparation and CNN training to model evaluation and a web-based prediction interface.

✨ Features

🖼️ MRI Image Upload — Upload an image through the Streamlit interface.

🧠 CNN-Based Classification — Predict one of two classes: tumor or no tumor.

📊 Confidence Display — Show the model score associated with the prediction.

🔄 Image Preprocessing — Resize images to the model's expected input dimensions.

🧪 Data Augmentation — Use random flips, rotations, and zoom during training.

📈 Model Evaluation — Generate accuracy/loss plots, a classification report, and a confusion matrix.

🌐 Interactive Web App — Explore predictions through a simple browser-based interface.

💾 Model Export — Save the trained model in Keras .keras format.

🖥️ Application Preview

The app provides an image-upload panel, an MRI preview, and a prediction panel.

<!--
Add your screenshots to a screenshots/ directory and update these paths.

![No-tumor prediction](screenshots/no-tumor-preview.png)
![Tumor prediction](screenshots/tumor-preview.png)
-->

🛠️ Tech Stack

Technology

Purpose



Core programming language



Deep-learning framework



CNN model construction and training



Web application interface



Image processing



Numerical operations



Training plots and visualization



Evaluation metrics



Dataset source

📂 Dataset

This project notebook downloads the Brain MRI Images for Brain Tumor Detection dataset using KaggleHub.

🔗 Dataset: Brain MRI Images for Brain Tumor Detection on Kaggle

The notebook expects the image dataset to contain class folders commonly named yes and no. The dataset directory and class counts are discovered during execution.

Dataset split

🏋️ Training: 80%

🧪 Validation: 20%

🔁 Random seed: 42

Note: The notebook uses a training/validation split and does not define a separate independent test set. Validation metrics should not be presented as independent test results.

🧠 Model Architecture

The notebook builds a CNN using TensorFlow/Keras.

Component

Configuration

Input size

224 × 224 × 3

Data augmentation

Random horizontal/vertical flips, rotation, and zoom

Normalization

Rescale pixel values to [0, 1]

Convolutional layers

32, 64, and 128 filters

Pooling

Max pooling

Dense layer

128 units with ReLU

Dropout

0.5

Output layer

1 sigmoid unit

Optimizer

Adam

Loss function

Binary cross-entropy

Metric

Accuracy

Batch size

32

Epochs

5

These values describe the current notebook configuration. They do not guarantee clinical accuracy or performance on images from other sources.

📁 Project Structure

A suggested GitHub repository structure:

brain-tumor-detection/
│
├── 📓 Brain_Tumor_Detection.ipynb
├── 🐍 app.py
├── 💾 brain_tumor_model.keras
├── 📄 requirements.txt
├── 📘 README.md
└── 📁 screenshots/
    ├── no-tumor-preview.png
    └── tumor-preview.png

The notebook generates app.py and saves the trained model as brain_tumor_model.keras. Make sure the model file is present before launching the app. If you do not include the model in the repository, document how users can obtain it.

⚙️ Installation

1️⃣ Clone the repository

git clone <YOUR_REPOSITORY_URL>
cd brain-tumor-detection

Replace <YOUR_REPOSITORY_URL> with your GitHub repository URL.

2️⃣ Create a virtual environment

Windows

python -m venv .venv
.venv\Scripts\activate

macOS / Linux

python3 -m venv .venv
source .venv/bin/activate

3️⃣ Install dependencies

Create a requirements.txt file:

tensorflow
streamlit
numpy
Pillow
opencv-python
matplotlib
seaborn
scikit-learn
kagglehub

Install the dependencies:

pip install -r requirements.txt

💡 For reproducible environments, test your setup and pin compatible dependency versions.

🚀 Run the Application

Ensure app.py and brain_tumor_model.keras are in the same directory.

streamlit run app.py

Then:

🌐 Open the local URL shown in your terminal.

📤 Upload a brain MRI image.

🖼️ Review the uploaded image.

🔍 Read the model-generated prediction and confidence score.

🧮 How the prediction threshold works

The application uses a sigmoid output and a threshold of 0.5:

Output > 0.5 → Tumor Detected

Output ≤ 0.5 → No Tumor Detected

For the no-tumor result, the app displays 1 - model_output as the confidence score. These values are model scores, not calibrated clinical probabilities.

📊 Model Evaluation

The notebook includes:

📈 Training and validation accuracy curves

📉 Training and validation loss curves

🧾 Classification report

🧩 Confusion matrix

No benchmark accuracy is claimed here. Add the metrics from your actual training run only after verifying them, and clearly state which dataset split was used.

🔮 Future Improvements

🧪 Add a separate, patient-independent test set and external validation.

📊 Report precision, recall, F1-score, sensitivity, and specificity.

🧠 Compare the baseline CNN with transfer-learning models.

🧹 Investigate class imbalance, data leakage, and dataset quality.

🛡️ Improve upload validation and error handling.

📦 Track model versions and document reproducible experiments.

🎨 Improve the interface's accessibility and responsive layout.

🤝 Contributing

Contributions and suggestions are welcome!

Fork the repository.

Create a feature branch.

Commit your changes.

Open a pull request describing your improvements.

For significant changes, open an issue first to discuss the proposal.

⚠️ Medical Disclaimer

This project is intended for educational and experimental purposes only.

It is not a medical device, is not clinically validated, and must not be used to diagnose or rule out a brain tumor or to make treatment decisions. Model predictions may be incorrect. Always consult a qualified medical professional for MRI interpretation and medical advice.

📄 License

No license is specified yet. Add a LICENSE file to clarify the permissions for using, modifying, and distributing this project.

<div align="center">

💙 Built to explore Deep Learning, Computer Vision, and Medical Image Classification

If you find this project useful, consider giving the repository a ⭐

</div>
