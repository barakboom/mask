
mask-detection/
│
├── dataset/
│   ├── train/
│   │   ├── with_mask/
│   │   └── without_mask/
│   └── test/
│       ├── with_mask/
│       └── without_mask/
│
├── mask_detection.ipynb   # Colab notebook
├── mask_model.h5          # Saved trained model
├── README.md              # Project documentation
└── app.py (optional)      # Gradio interface script

## 📥 Dataset

You must prepare the dataset in this folder format
dataset/
   train/
      with_mask/
      without_mask/
   test/
      with_mask/
      without_mask/

You can use any public face mask dataset (Kaggle recommended).

## 🧠 Model Architecture

A simple **Convolutional Neural Network (CNN)**:

* 3× Conv2D layers
* 3× MaxPooling2D layers
* Flatten layer
* Dense(128) layer
* Dense(1, sigmoid) output

Designed for fast training even on low-end hardware.

## 🚀 How to Train the Model (Google Colab)

1. Upload the `dataset/` folder to Colab
2. Open the notebook: `mask_detection.ipynb`
3. Run all cells:

   * Install packages
   * Load dataset
   * Train model
   * Plot accuracy/loss
   * Launch Gradio demo

Training time: **5–15 minutes** depending on GPU.

## 📊 Evaluation

You will get:

* **Training accuracy**
* **Validation accuracy**
* **Loss curves**

Example (expected):

* Training Accuracy: **95%**
* Validation Accuracy: **90–93%**

## 🖼️ Gradio Demo (Real-Time Testing)

Once training is done, run:

```python
iface.launch()
```

This opens a browser interface where you can upload any face image.

Outputs probabilities:

* `Mask: 0.95` → Mask detected
* `No Mask: 0.87` → No mask detected

---

## 💾 Saving and Loading Model

Save model:

```python
model.save('mask_model.h5')
```

Load model later:

```python
model = tf.keras.models.load_model('mask_model.h5')
```

--

## 📤 How to Upload to GitHub (Simple)

### Method: Upload from Google Drive

1. Save notebook + model into Google Drive
2. Go to GitHub → New Repo
3. Click **Upload files**
4. Select your files
5. Commit and done


## 👨‍💻 Authors

* Course: Selected Topics in Computer Science (CoSc4132)
Group Member                                                        ID
1.Abebe Mamuye………………………………. 0699/13 
2.Bereket Negassa ………………………………0709/13 
3.Dagmawi Dereje ………………………………0723/13 
4.Mekonnen Shawatatek ……………………… ..0760/13 
5.Rediet Habtamu ………………………………...0768/13 
6.Tadiyos Mamush ………………………………..0776/13
