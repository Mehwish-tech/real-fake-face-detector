# Real vs Fake Face Detector

A deep learning project to classify images as **real** or **AI-generated (fake)** faces, built as a 4-member team project.

## 📁 Project Structure

```
real-fake-face-detector/
├── data/                              # dataset (not pushed to GitHub — too large)
├── notebooks/
│   ├── 01_data_preprocessing.ipynb    — Data loading & preprocessing
│   ├── 02_model_training.ipynb        — Model building & training
│   ├── 03_evaluation.ipynb            — Evaluation & graphs
│   └── 04_deployment.ipynb            — Deployment / final integration
├── models/                            # saved trained models (.keras)
├── outputs/                           # accuracy/loss graphs, confusion matrix images
├── requirements.txt
├── .gitignore
└── README.md
```


## ⚙️ Setup

```bash
git clone https://github.com/<your-username>/real-fake-face-detector.git
cd real-fake-face-detector

python3 -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

pip install -r requirements.txt
```

## ▶️ How to Run

Run the notebooks **in order**, since each one depends on the outputs of the previous:

1. `01_data_preprocessing.ipynb` — loads and prepares the dataset, creates `train_ds` / `val_ds` / `test_ds`
2. `02_model_training.ipynb` — builds and trains the model, produces `model` and `history`
3. `03_evaluation.ipynb` — evaluates the model, generates accuracy/loss graphs and confusion matrix, saves `real_fake_model.keras` and `class_names.json`
4. `04_deployment.ipynb` — loads the saved model for final use/deployment

## 📦 Trained Model

The trained model file (`models/real_fake_model.keras`) is large and may not be tracked directly in GitHub. If using Git LFS:

```bash
git lfs install
git lfs track "*.keras"
```

Otherwise, share it via a cloud link and note the link here.

## 📊 Results

_(Add final accuracy, loss, and confusion matrix screenshots here once evaluation is complete.)_

## 📝 Notes

- Make sure `class_names` order matches between training and evaluation notebooks.
- Run notebooks in the same Python environment (see `requirements.txt`) to avoid version mismatches.
