# 📘 GPA Tahmini: İleri ve Geri Yayılım Yöntemi (Elle Kodlama)

Bu çalışma, **Student Performance Dataset** kullanılarak öğrencilerin genel not ortalamasını (GPA) tahmin etmeyi amaçlamaktadır. Bu süreçte, **ileri yayılım (forward propagation)** ve **geri yayılım (backward propagation)** adımları **elle (sıfırdan)** Python/NumPy dışında kütüphane kullanılmadan gerçekleştirilmiştir.

---

## 🧪 Uygulanan Adımlar

### 1️⃣ Veri Hazırlama ve Ön İşleme
- Kullanılan dosya: `5_ForwardAndBackwardPropagation.ipynb`
- Özellikler (`X`) ve hedef (`y`) sütunları seçildi.
- `StudentID` gibi gereksiz sütunlar çıkarıldı.
- **Elle normalizasyon** (z-score) uygulandı:


### 2️⃣ Model Mimarisi
- Giriş katmanı: Tüm özellikler
- **Gizli katman**: 8 nöron, ReLU aktivasyon
- Çıkış katmanı: GPA tahmini

### 3️⃣ İleri Yayılım (Forward Propagation)
- `Z1 = X @ W1 + b1`, `A1 = relu(Z1)`
- `Z2 = A1 @ W2 + b2` (tahminler)

### 4️⃣ Kayıp Hesaplama
- Kullanılan metrik: **Ortalama Kare Hata (MSE)**

### 5️⃣ Geri Yayılım (Backward Propagation)
- Gradyanlar hesaplandı: `dW1`, `db1`, `dW2`, `db2`
- Öğrenme oranı (`lr`) ile parametreler güncellendi.

### 6️⃣ Eğitim Döngüsü
- **Epoch sayısı:** 1000
- **Her 100 iterasyonda** loss değeri yazdırıldı.

---

## 📊 Görselleştirmeler

- **Kayıp (Loss) - Epoch Eğrisi**: Eğitim süresince modelin kayıp değerlerinin azalmasını gösterir.
- ![image](https://github.com/user-attachments/assets/9d6c8357-fa12-4d69-b27a-fd5f89cd4bb8)
  
- **Gerçek ve Tahmin Karşılaştırması**: Gerçek GPA değerleri ile tahmin edilen değerler karşılaştırıldı.
![image](https://github.com/user-attachments/assets/04000069-fa41-44ca-bb3e-e0f59593f3bd)

- **Hata Dağılımı Grafiği**: Modelin yaptığı tahmin hatalarının dağılımını gösterir.

![image](https://github.com/user-attachments/assets/ee30b73c-ed23-4446-a208-d6f358b120de)

---

## 🔍 Sonuç ve Karşılaştırma

| Özellik           | Değer                                       |
|------------------|---------------------------------------------|
| Model Türü       | Elle kodlanmış yapay sinir ağı (1 gizli katman) |
| Aktivasyon       | ReLU (gizli katman)                          |
| Öğrenme Oranı    | 0.01                                        |
| Epoch Sayısı     | 1000                                        |
| Son Hata (MSE)   | ~0.1277                                     |
| Görseller        | Kayıp eğrisi, tahmin ve hata dağılımı grafikleri |

Model, veri setine uyum sağlayarak GPA tahminini başarılı şekilde gerçekleştirmiştir.

---

## 📁 Klasör ve Dosyalar

- `5_ForwardAndBackwardPropagation.ipynb`: Elle kodlanmış ileri ve geri yayılım algoritması uygulaması
- `student-performance.csv`: Kullanılan veri seti (indirme bağlantısı yoksa eklenecek)
- 'verionisleme.ipynb' : Veri ön işleme dosyası.
---

## 🔗 Kaynaklar

- [NumPy Documentation](https://numpy.org/doc/stable/)
- [Machine Learning Mastery - ReLU Activation](https://machinelearningmastery.com/rectified-linear-activation-function-for-deep-learning-neural-networks/)
- [Forward ve Backward Propagation Kaynakları](https://towardsdatascience.com/forward-and-backward-propagation-explained-137024d7c1e0)

---
