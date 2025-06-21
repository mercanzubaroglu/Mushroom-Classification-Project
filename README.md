# 🍄 Mushroom Classification with Machine Learning

Bu projede, mantarların fiziksel özelliklerine göre **zehirli (poisonous)** ya da **yenilebilir (edible)** olup olmadığını tahmin eden bir makine öğrenmesi modeli geliştirilmiştir.  
In this project, a machine learning model is developed to predict whether a mushroom is **poisonous** or **edible**, based on its physical characteristics.

---

## 📁 Dataset (Veri Kümesi)

- **Kaynak / Source:** [UCI Machine Learning Repository – Mushroom Dataset](https://archive.ics.uci.edu/ml/datasets/Mushroom)
- **Gözlem Sayısı / Number of Instances:** 8124
- **Özellik Sayısı / Number of Features:** 22 (hepsi kategorik / all categorical)

Veri kümesi; mantarın şapkası, rengi, kokusu, sap yapısı gibi fiziksel özelliklerini içerir.  
The dataset includes features such as cap shape, cap color, odor, stalk characteristics, and more.

---

## 🧪 Technologies & Libraries (Kütüphaneler)

- Python
- pandas, numpy (veri işleme / data processing)
- matplotlib, seaborn (görselleştirme / visualization)
- scikit-learn (makine öğrenmesi / machine learning)
- LabelEncoder (kategorik veriler için / for encoding categorical variables)
- RandomForestClassifier (sınıflandırma modeli / classification model)

---

## 🔎 Data Preprocessing (Veri Ön İşleme)

- `'?'` karakteriyle temsil edilen eksik veriler `NaN` ile değiştirildi ve mod değeriyle dolduruldu.  
  Missing values represented with `'?'` were converted to `NaN` and filled using the mode.

- Tüm sütunlar kategorik olduğu için `LabelEncoder` ile sayısallaştırıldı.  
  All features were label-encoded since they are categorical.

---

## 📊 Data Visualization (Veri Görselleştirmesi)

- Sınıf dağılımı analiz edildi (zehirli vs yenilebilir).  
  Class distribution was analyzed (poisonous vs edible).

- Özellikle `odor`, `gill-size`, `spore-print-color` gibi özelliklerin sınıflandırma için çok belirleyici olduğu görüldü.  
  Features like `odor`, `gill-size`, and `spore-print-color` were found to be highly important.

- Korelasyon matrisi çıkarılarak değişkenler arası ilişkiler incelendi.  
  A correlation heatmap was used to explore feature relationships.

---

## 🤖 Modeling (Modelleme)

Model olarak `RandomForestClassifier` kullanılmıştır.  
Random Forest Classifier was selected as the model.

Veri seti %80 eğitim, %20 test olarak bölünmüştür.  
The dataset was split into 80% training and 20% test sets.

**Model Performansı / Model Performance:**

| Metric        | Değer / Value | Açıklama (Türkçe)                  | Explanation (English)                  |
|---------------|---------------|----------------------------------|--------------------------------------|
| Accuracy      | 100%          | Doğruluk: Doğru tahmin oranı     | Accuracy: Ratio of correct predictions |
| Precision     | 1.00          | Kesinlik: Pozitif tahminlerin doğruluğu | Precision: Accuracy of positive predictions |
| Recall        | 1.00          | Duyarlılık: Gerçek pozitifleri yakalama oranı | Recall: Ability to find all positive cases |
| F1-Score      | 1.00          | F1 Skoru: Precision ve Recall’un harmonik ortalaması | F1-Score: Harmonic mean of Precision and Recall |

---

## 📈 Feature Importances (Özellik Önem Skorları)

Modelin kararlarında en etkili değişkenler:  
Top features in the model:

- `odor`
- `gill-size`
- `spore-print-color`
- `stalk-root`

Bu analiz, modelin kararlarının nasıl oluştuğunu anlamada önemli katkı sağlar.  
This analysis helps us interpret how the model makes its predictions.

---
