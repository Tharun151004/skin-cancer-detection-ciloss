# 🩺 Skin Cancer Detection using VGG16 + Custom Loss (CILoss)

## 📌 Overview
This project focuses on **skin lesion classification** (cancerous vs. non-cancerous) using the **ISIC 2024 Challenge dataset**.  
We implement **transfer learning with VGG16** and introduce a **custom imbalance-aware loss function (CILoss)** to improve sensitivity for minority (cancerous) cases.

---

## 📂 Project Structure
- `custom-loss-2-0.ipynb` → Main training & evaluation notebook  
- `results/` → Confusion matrices, classification reports, misclassification CSVs  
- `report/` → Kaggle competition details & methodology  

---

## ⚙️ Methodology
1. **Dataset** – ISIC 2024 skin cancer dataset (cancerous vs. non-cancerous).  
2. **Model** – Fine-tuned **VGG16** for binary classification.  
3. **Custom Loss (CILoss)** – Designed to handle class imbalance using adaptive weighting.  
4. **Evaluation** – Compared CILoss with CrossEntropyLoss using accuracy, precision, recall, F1-score.  

---

## 📊 Results
| Loss Function    | Test Accuracy | Sensitivity (Cancer Class) |
|------------------|---------------|-----------------------------|
| CrossEntropyLoss | 66.5%         | Lower                       |
| CILoss (Ours)    | 70.8%         | Improved cancer detection   |

✅ Achieved **+4.3% accuracy improvement** over baseline.  
✅ Enhanced **recall for minority class (cancerous lesions)** → crucial for medical applications.  

---

## 💡 Applications
- Early skin cancer detection & clinical decision support  
- Assisting dermatologists in diagnostic screening  
- AI-driven healthcare solutions  

---

## 🚀 How to Run
```bash
# Clone repo
git clone https://github.com/Tharun151004/skin-cancer-detection-ciloss.git
cd skin-cancer-detection-ciloss

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook custom-loss-2-0.ipynb

