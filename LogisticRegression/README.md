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

Bu proje kapsamında Mushroom veri seti kullanılarak iki farklı Logistic Regression modeli başarıyla uygulanmıştır:

### 🔹 **Scikit-Learn Logistic Regression**
- Yüksek doğruluk (%96) elde edilmiştir.
- Eğitim ve test süreleri oldukça kısadır.
- Zehirli mantar sınıfı için **Recall** oranı %93 olup güvenli bir sınıflandırma başarısı göstermiştir.
- Gerçek hayatta kullanılabilir, optimize bir modeldir.

### 🔹 **Manuel Logistic Regression (Gradient Descent)**
- Model %93 doğruluk sağlamıştır.
- Zehirli sınıf için **Recall %89** olup sınıflandırma başarısı biraz daha düşük kalmıştır.
- Eğitim süresi daha uzundur çünkü ağırlık güncelleme işlemleri elle yapılmıştır.
- Özellikle zehirli sınıftaki False Negative (yanlış yenilebilir sınıflama) riski artmıştır.

### 🚀 **Genel Yorum ve Sonuç**
- Scikit-Learn modeli pratik kullanım ve güvenilirlik açısından önde gelmiştir.
- Manuel model algoritmanın temellerini öğrenmek ve nasıl çalıştığını anlamak için faydalıdır.
- Ancak kritik problemler için **Scikit-Learn tercih edilmelidir** çünkü recall değerleri daha yüksektir ve güvenli sonuçlar sağlar.
- Zehirli sınıfta recall oranı kritik olduğu için Scikit-Learn modeli gerçek hayattaki senaryolarda kullanılabilir.
- Manuel modelde, daha fazla iterasyon, öğrenme oranı ayarı ve feature engineering ile performans iyileştirilebilir.

  
---

### **Değerlendirme Metriklerinin Seçiminde Problem ve Sınıf Dağılımının Önemli midir?**  
Evet, değerlendirme metriklerinin seçimi problem tipi ve sınıf dağılımı açısından oldukça kritiktir.
Problem Tipi Açısından;eğer sınıflandırma problemi ikiden fazla sınıfa (multi-class) sahipse, performans metrikleri her bir sınıf için ayrı ayrı hesaplanmalı ve detaylı şekilde değerlendirilmelidir. Böylece modelin hangi sınıflarda güçlü, hangi sınıflarda zayıf olduğu daha net ortaya konur.
Sınıf Dağılımı Açısından; sınıf dağılımı dengesiz olduğunda, yalnızca doğruluk (accuracy) metriğine bakmak yanıltıcı sonuçlar verebilir.
Örneğin, eğer veri setinizde sınıf dağılımı dengesiz ise, yani bir sınıf diğerine göre çok daha fazla örneğe sahipse, doğruluk metriği yanıltıcı olabilir. Bu durumda, duyarlılık ve kesinlik gibi metrikler daha anlamlı sonuçlar sağlayabilir. Bu nedenle, projenizde sınıf dağılımını dikkate alarak değerlendirme metriklerini seçmeniz ve yorumlamanız, modelinizin gerçek performansını daha doğru bir şekilde yansıtacaktır.
