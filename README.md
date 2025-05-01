# NFT Music Price Prediction

This project uses machine learning regression and classification models to predict the **NFT_LAST_PRICE** of music-based NFTs based on metadata, collection-level, and owner-level attributes. Four development phases were implemented using **AdaBoost** and **Random Forest** algorithms.

---

## 📁 Dataset
The dataset used: `Training_dataset_Cleaned_all_phasses_updated.csv`
- Includes NFT metadata (e.g., first price, sale count)
- Collection details (e.g., average price, ceiling price)
- Owner-related features (e.g., total purchases, diversity)
- Timestamps processed into hour/day/month

---

## 🔧 Tools and Technologies
- **Languages**: Python
- **Libraries**: `pandas`, `numpy`, `scikit-learn`, `matplotlib`
- **Models**: `RandomForestRegressor`, `AdaBoostRegressor`, `RandomForestClassifier`, `AdaBoostClassifier`
- **Normalization**: `MinMaxScaler`
- **Encoding**: `LabelEncoder`

---

## 🧠 Model Phases and Features
### Phase 1: NFT Metadata Only
- Features: `TOKEN_ID`, `NFT_FIRST_PRICE`, `NFT_AVG_PRICE`, `NFT_SALE_COUNT`

### Phase 2: NFT + Collection Information
- Adds: `CONTRACT_ADDRESS`, `COLLECTION_AVG_PRICE`, `COLLECTION_CEILING_PRICE`, `TOTAL_VOLUME_USD`

### Phase 3: NFT + Owner Information
- Features include owner purchases, diversity, and time features (`SALE_HOUR`, `SALE_DAY`, `SALE_MONTH`)

### Phase 4: Combined All Features
- Merges all features from Phases 1–3

---

## 📊 Evaluation Metrics
- **Regression**: R², RMSE, MAE
- **Classification**: ROC AUC, F1 Score, Precision, Recall

---

## ✅ Results Summary
All models were evaluated using both train/test splits and 5-fold cross-validation.

### 📉 Regression Results:
- AdaBoost performed better for early phases.
- Random Forest had stronger performance with more complex data (Phases 3 & 4).
- Visual comparisons using RMSE and R² graphs across all four phases are included.

### 📈 Classification (Phase 4):
- Used a binary label (high/low price based on median).
- ROC Curve plotted for Random Forest and AdaBoost classifiers.

---

## 📂 Repository Structure
```
├── data/
│   └── Training_dataset_Cleaned_all_phasses_updated.csv
├── notebooks/
│   └── regression_phase1_to_4.ipynb
│   └── classification_phase4.ipynb
├── outputs/
│   └── model outputs
│   └── ROC_curve_plot.png
├── README.md
```

---

## 📌 How to Run
1. Clone the repository
```bash
   git clone https://github.com/<your-username>/NFT_Music_Price_Prediction.git
```
2. Install dependencies
```bash
   pip install -r requirements.txt
```
3. Run each phase notebook in order under `/notebooks`

---

## 📘 Future Improvements
- Use advanced models like XGBoost or LightGBM
- Integrate real-time NFT market feeds
- Deploy as a web-based prediction app

---

## 👩‍💻 Author
**Haleema Malik**  
Final Year Software Engineering Student, Liverpool John Moores University

---

## 📜 License
This project is open-source and available under the MIT License.

---

## 📞 Contact
For questions or collaborations:
- Email: haleemamalik589@gmail.com
- GitHub: [@Haleema33](https://github.com/Haleema33)
