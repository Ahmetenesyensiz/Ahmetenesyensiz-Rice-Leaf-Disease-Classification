
# 🍚 Rice Leaf Disease Classification with Deep Learning

This project aims to classify rice leaf diseases using four state-of-the-art pre-trained deep learning models: **Xception**, **VGG16**, **MobileNet**, and **ResNet50**. The goal is to help automate disease identification in agricultural settings by leveraging computer vision techniques.

## 📁 Dataset

- **Source**: [Kaggle - Rice Leaf Disease Dataset](https://www.kaggle.com/datasets/nirmalsankalana/rice-leaf-disease-image)
- **Classes**: Bacterial Blight, Blast, Brown Spot, Tungro
- **Total Images**: 5,932
- **Split**: 80% Training / 20% Testing

## 🧠 Models Used

All models are based on pre-trained CNN architectures from Keras (ImageNet weights) and fine-tuned for 4-class classification:

- ✅ Xception
- ✅ VGG16
- ✅ MobileNet
- ✅ ResNet50

## 🔧 Techniques Applied

- **Transfer Learning**
- **Image Augmentation** (rotation, zoom, flip, etc.)
- **EarlyStopping and ModelCheckpoint**
- **Categorical Crossentropy Loss with Adam Optimizer**

## 📊 Results

| Model     | Accuracy | Precision | Recall | F1 Score |
|-----------|----------|-----------|--------|----------|
| MobileNet | 0.99     | 0.99      | 0.99   | 0.99     |
| Xception  | 0.98     | 0.98      | 0.98   | 0.98     |
| ResNet50  | 0.82     | 0.84      | 0.82   | 0.83     |
| VGG16     | 0.87     | 0.87      | 0.87   | 0.87     |

> 🔎 MobileNet achieved the best performance with the shortest training time (~27 minutes).

## 📈 Visualizations

- 📌 Training and Validation Accuracy/Loss plots  
- 📌 Confusion Matrices for each model  
- 📌 Comparative Performance Table  
- 📌 Training Time Comparison

## 💡 Future Work

- Integration into real-time mobile or embedded systems  
- Testing on broader datasets with more disease classes  
- Extending to different plant types

## 👨‍💻 Contributors

- Ahmet Enes Yensiz – [@Ahmetenesyensiz](https://github.com/Ahmetenesyensiz)  
- Kemal Kerem Acar

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/Ahmetenesyensiz/Ahmetenesyensiz-Rice-Leaf-Disease-Classification

# 2. Navigate into project
cd Ahmetenesyensiz-Rice-Leaf-Disease-Classification

# 3. (Optional) Setup virtual environment
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows

# 4. Install requirements
pip install -r requirements.txt

# 5. Run Jupyter Notebook
jupyter notebook rice_leaf_classifier.ipynb
```

## 📄 License

This project is for academic use under the MIT license.
