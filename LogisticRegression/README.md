# 📝 Logistic Regression - Binary Classification Project (YZM212 Lab 2)

## 🔎 Problem Tanımı
Bu proje kapsamında, Mushroom dataset kullanılarak mantarların zehirli veya yenilebilir olup olmadığı Logistic Regression modeliyle tahmin edilmiştir.

**Amaç:** Hem Scikit-Learn hem de Manuel Logistic Regression modellerini eğitip karşılaştırmak.

---

## 📂 Veri Seti Bilgisi
- Kaynak: [UCI Mushroom Dataset](https://archive.ics.uci.edu/ml/datasets/Mushroom)
- Örnek Sayısı: 8124
- Özellik Sayısı: 22 (tamamı kategorik)
- Hedef Değişken: `class` (p - poisonous, e - edible)
- Eksik Veriler temizlenmiştir (stalk-root '?' satırları drop edilmiştir).
- Kategorik veriler **Label Encoding** ile sayısallaştırılmıştır.

---

## 🛠 Uygulanan Yöntemler

### ✅ Scikit-Learn Logistic Regression
- `LogisticRegression(max_iter=200)`
- Eğitim ve test süreleri ölçüldü
- Classification report ve confusion matrix hesaplandı

### ✅ Manuel Logistic Regression (Gradient Descent)
- Sigmoid fonksiyon ve Binary Cross Entropy Loss elle yazıldı
- Ağırlıklar Gradient Descent ile güncellendi
- Performans değerlendirmesi yapıldı

---

## 📈 Performans Karşılaştırması

| Model                    | Accuracy | Eğitim Süresi | Test Süresi |
|--------------------------|---------|-------------|------------|
| **Scikit-Learn**         | 0.9601  | 0.1291 s    | 0.0028 s   |
| **Manuel Logistic**      | 0.9327  | 0.7386 s    | 0.0004 s   |

---

## 📌 Önemli Metrikler

| Metric       | Scikit-Learn | Manuel Logistic |
|------------- |-------------|-----------------|
| **Precision (Class 1)** | 0.96 | 0.93 |
| **Recall (Class 1)**    | 0.93 | 0.89 |
| **F1-Score (Class 1)**  | 0.95 | 0.91 |

⚠️ Manuel modelde zehirli sınıfa ait recall değeri düştüğü için **false negative riski** artmıştır.

---

## ⚖ Teorik Karşılaştırma

| Kriter           | Scikit-Learn       | Manuel Logistic |
|------------------|--------------------|-----------------|
| Kullanım         | Kolay              | Zor (elle yazıldı) |
| Eğitim Hızı      | Hızlı              | Daha yavaş      |
| Doğruluk         | Yüksek             | Biraz daha düşük |
| Esneklik         | Düşük              | Yüksek (özelleştirilebilir) |

---

## 📊 Sonuç ve Yorumlar
- Scikit-Learn modeli hız ve doğruluk açısından öne çıkmıştır.
- Manuel model teorik öğrenme için faydalıdır ancak riskli sınıflarda recall kaybı yaşanmıştır.
- **Recall (Class 1)** - Zehirli sınıf için kritik olup, gerçek hayatta en önemli metriktir.
- Class imbalance sorunu yoktur, sınıflar dengelidir.

---
