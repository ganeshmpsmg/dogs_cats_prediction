# dogs_cats_prediction
🐾 Prodigy Infotech — Machine Learning Intern | Task 3
<div align="center">
🐶 Dogs vs Cats — Image Classification using CNN 🐱

<br/>

Internship Program · Prodigy Infotech · Machine Learning · Task 3 of 5

</div>

🏢 Internship Details
FieldDetails🏛️ OrganizationProdigy Infotech👨‍💻 RoleMachine Learning Intern📋 TaskTask 3 — Image Classification (Dogs vs Cats)🧠 DomainComputer Vision · Deep Learning · CNN🔗 GitHubgithub.com/your-username/PRODIGY_ML_03

📌 Task Description

Build an image classification model to distinguish between images of cats and dogs using a Convolutional Neural Network (CNN).

This task is part of the Prodigy Infotech Machine Learning Internship and focuses on core computer vision concepts including image preprocessing, data augmentation, model building, training, and evaluation.

🗂️ Dataset
PropertyValueNameDogs vs CatsSourceKaggle — moazeldsokyx/dogs-vs-catsClassescat · dogTypeBinary Image ClassificationFormatJPEG images in labeled subdirectories
pythonimport kagglehub
path = kagglehub.dataset_download("moazeldsokyx/dogs-vs-cats")

📁 Project Structure
PRODIGY_ML_03/
│
├── 📓 dogs_vs_cats_pipeline.ipynb    ← Main notebook (all 10 steps)
├── 📄 requirements.txt               ← Python dependencies
├── 📄 README.md                      ← Project documentation
│
├── 💾 dogs_vs_cats_model.h5          ← Saved model (after training)
│
└── 📂 assets/
    └── 🖼️  sample_predictions.png    ← Sample output (optional)

🧠 Model Architecture
Input (128 × 128 × 3)
        │
        ▼
┌─────────────────────┐
│  Conv2D 32 filters  │  ← 3×3 kernel, ReLU
│  MaxPooling2D       │
└─────────────────────┘
        │
        ▼
┌─────────────────────┐
│  Conv2D 64 filters  │  ← 3×3 kernel, ReLU
│  MaxPooling2D       │
└─────────────────────┘
        │
        ▼
┌─────────────────────┐
│  Conv2D 128 filters │  ← 3×3 kernel, ReLU
│  MaxPooling2D       │
└─────────────────────┘
        │
        ▼
    Flatten
        │
        ▼
  Dense (128) ReLU
        │
   Dropout (0.5)
        │
        ▼
  Dense (1) Sigmoid
        │
        ▼
  Output: Cat / Dog

Loss Function: Binary Crossentropy
Optimizer: Adam
Evaluation Metric: Accuracy


⚙️ Pipeline — Step by Step
#StepDescription1Install & ImportSet up all libraries and dependencies2Download DatasetDownload via kagglehub, explore folder structure3PreprocessingRescale pixels, apply augmentation, 80/20 split4Visualize SamplesDisplay 8 labeled sample images5Build CNN ModelDefine architecture with Conv + Dense layers6Train ModelFit with EarlyStopping + ReduceLROnPlateau7Plot CurvesAccuracy & loss graphs for train vs validation8EvaluateClassification report + confusion matrix9PredictClassify any single custom image10Save & LoadExport model as .h5 for reuse

🚀 Getting Started
1️⃣ Clone the Repository
bashgit clone https://github.com/your-username/PRODIGY_ML_03.git
cd PRODIGY_ML_03
2️⃣ Install Dependencies
bashpip install -r requirements.txt
3️⃣ Launch the Notebook
Jupyter:
bashjupyter notebook dogs_vs_cats_pipeline.ipynb
PyCharm:
Open PyCharm → File → Open → select PRODIGY_ML_03/
Right-click dogs_vs_cats_pipeline.ipynb → Open in Jupyter Notebook

📊 Results
MetricScoreTraining Accuracy~92%Validation Accuracy~88%OptimizerAdamLossBinary CrossentropyCallbacksEarlyStopping · ReduceLROnPlateau

Results may vary slightly based on system, seed, and number of epochs.


🖼️ Sample Prediction Output
pythonpredict_image("/path/to/test.jpg")

# ┌──────────────────────────┐
# │  Prediction: Dog 🐶      │
# │  Confidence:  94.3%      │
# └──────────────────────────┘

🛠️ Tech Stack
LibraryPurposetensorflow / kerasModel building & trainingnumpyArray operationsmatplotlibVisualizationscikit-learnEvaluation metricskagglehubDataset downloadPillowImage loading & processing


📄 License
This project is licensed under the MIT License.
See the LICENSE file for full details.

👤 Author
<div align="center">
  
</div>

<div align="center">
⭐ If you found this helpful, please star the repository!
Made with ❤️ during the Prodigy Infotech Machine Learning Internship
Show Image
</div>
