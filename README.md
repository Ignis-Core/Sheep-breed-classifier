🐑 Sheep Breed Classifier
A deep learning project that classifies sheep breeds from images using transfer learning with EfficientNetB3, built and trained on Google Colab with GPU support.

📌 Overview
This project uses a pre-trained EfficientNetB3 model fine-tuned on a custom sheep breed dataset. It includes a full ML pipeline — from data loading and augmentation to evaluation and a live Gradio web UI for real-time predictions.

🚀 Features

✅ Transfer learning with EfficientNetB3
✅ Two-phase fine-tuning (head training → full fine-tuning)
✅ On-the-fly data augmentation
✅ Class imbalance handling via class weights
✅ Confusion matrix & classification report
✅ Test-Time Augmentation (TTA) for better accuracy
✅ Interactive Gradio UI for live predictions


🗂️ Dataset Structure
Store your dataset in Google Drive in this format:
MyDrive/
└── sheep/
    ├── breed_1/
    │   ├── img1.jpg
    │   └── img2.jpg
    ├── breed_2/
    │   ├── img1.jpg
    │   └── img2.jpg
    └── ...

🛠️ Tech Stack
ToolPurposeTensorFlow / KerasModel building & trainingEfficientNetB3Pre-trained base modelOpenCVImage reading & validationScikit-learnMetrics & evaluationMatplotlibVisualizationsGradioInteractive prediction UIGoogle ColabCloud GPU training

▶️ How to Run

Open the notebook in Google Colab
Mount your Google Drive
Place your sheep dataset under MyDrive/sheep/
Run all cells top to bottom
Use the Gradio UI at the end to test predictions


📊 Model Architecture
Input Image (300x300)
      ↓
Data Augmentation
      ↓
EfficientNetB3 (pre-trained, ImageNet)
      ↓
Global Average Pooling
      ↓
Dense + Dropout
      ↓
Softmax Output (N breeds)

📈 Training Strategy

Phase A — Train only the classification head (base frozen)
Phase B — Unfreeze base and fine-tune with a lower learning rate
Callbacks — ModelCheckpoint, ReduceLROnPlateau, EarlyStopping


📁 File Structure
Sheep-breed-classifier/
├── sheep_finetune_EfficientNetB3.ipynb   # Main notebook
├── .gitignore                             # Ignores checkpoints & model files
└── README.md                             # This file

## 👥 Contributors

- **IgnisCore** (@Ignis-Core)
- **Nishuprocode** (@Nishuprocoder)

## 🔗 Repository

https://github.com/Ignis-Core/Sheep-breed-classifier

