# 📌 Naive Bayes ile Diyabet Tahmini 
#  Naive Bayes ile Diyabet Tahmini

Bu proje,2024 – 2025 Bahar Dönemi YZM212 Makine Öğrenmesi Dersi I. Laboratuvar Değerlendirmesi Kkapsamında yapılmıştır. **Naive Bayes algoritması** kullanarak **diyabet hastalığını tahmin etmeyi** amaçlamaktadır. Hem **Scikit-Learn'ün Gaussian Naive Bayes modeli** hem de **manuel olarak yazılan Naive Bayes modeli** karşılaştırılmıştır.

---

##  Proje İçeriği
- `veri_onisleme.ipynb`: **Veri temizleme ve ön işleme adımları** içeren Jupyter Notebook dosyası.
- `naiveBayes.ipynb`: **Manuel olarak yazılmış Naive Bayes modeli**.
- `gaussianNaiveBayesScikitLearn.ipynb`: **Scikit-Learn kütüphanesi ile oluşturulan Naive Bayes modeli**.
- `diabetes.csv`: **Orijinal veri seti**.
- `veri_temiz.csv`: **Ön işleme sonrası temizlenmiş veri seti**.
- `requirements.txt`: Proje için gerekli Python kütüphanelerini içeren dosya.
- `.gitignore`: Gereksiz dosyaları Git versiyon kontrolüne eklememek için kullanılan dosya.

---

## Kullanılan Yöntemler
Bu projede, **iki farklı yöntem** kullanılarak model eğitimi yapılmıştır:

1️⃣ **Scikit-Learn GaussianNB modeli**  
   - `from sklearn.naive_bayes import GaussianNB` kullanılarak uygulandı.  
   - Eğitim ve test süreleri hesaplandı.  
   - Modelin performansı `classification_report` ve `confusion_matrix` ile değerlendirildi.

2️⃣ **Manuel Gaussian Naive Bayes modeli**  
   - `numpy` kullanılarak sıfırdan Naive Bayes algoritması yazıldı.
   - Model, özelliklerin ortalama ve standart sapmasını kullanarak olasılık hesaplamaları yaptı.
   - Sonuçlar, Scikit-Learn modeli ile karşılaştırıldı.

---

## Sonuçlar ve Karşılaştırma

| Model | Doğruluk (Accuracy) | Precision (1) | Recall (1) | Eğitim Süresi | Test Süresi |
|--------|----------------|---------------|-----------|--------------|------------|
| **Scikit-Learn GaussianNB** | **%75** | %65 | %67 | **0.0136 sn** | **0.0031 sn** |
| **Manuel GaussianNB** | **%75** | %65 | %67 | **0.0015 sn** | **0.0144 sn** |

### ** Gözlemler:**
- **Doğruluk (Accuracy) değeri her iki model için de %75 olarak hesaplandı.**
- **Precision ve Recall değerleri iki modelde de benzer sonuçlar verdi.**
- **Scikit-Learn modeli daha hızlı tahmin yapıyor (0.0031 saniye), ancak manuel modelin test süresi biraz daha uzun (0.0144 saniye).**
- **Öğrenme süresi açısından, manuel model daha hızlı eğitildi (0.0015 saniye) ancak tahmin yaparken daha uzun sürdü.**

### ** Sonuç:**
- **Manuel yazılmış Naive Bayes modeli ile Scikit-Learn modeli benzer doğruluk değerleri elde etti.**
- **Eğer hız kritikse, Scikit-Learn modeli tercih edilebilir.**
- **Ancak eğitim süresi açısından bakıldığında, manuel modelin daha hızlı olduğu görülmektedir.**

---

##  Nasıl Çalıştırılır?
1️⃣ **Veri setini hazırlayın**: `veri_onisleme.ipynb` dosyasını çalıştırarak temizlenmiş veriyi oluşturunve indirin.  
2️⃣ **Modelleri çalıştırın**:
   - `gaussianNaiveBayesScikitLearn.ipynb` → **Scikit-Learn modelini eğitmek için**
   - `naiveBayes.ipynb` → **Kendi Naive Bayes modelinizi test etmek için**
   - 
3️⃣ **Sonuçları analiz edin**: Çıktıları karşılaştırarak hangi modelin daha iyi çalıştığını değerlendirin.

---

## 📌 Özet
Bu projede, **Gaussian Naive Bayes algoritması hem Scikit-Learn ile hem de manuel olarak uygulanmıştır**. Performans açısından benzer doğruluk sonuçları elde edilmiş olup, **Scikit-Learn modeli daha hızlı tahmin yaparken, manuel model daha hızlı eğitilmiştir**. Bu çalışma, **temel olasılık teorisini ve makine öğrenmesi modellerinin performans analizini anlamak için faydalı bir deney olmuştur**. 🚀
