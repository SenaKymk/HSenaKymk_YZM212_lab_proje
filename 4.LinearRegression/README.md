# 📘 Öğrenci Performansı Tahmini: Lineer Regresyon Yöntemleri Karşılaştırması

Bu çalışma, **Student Performance Dataset** kullanılarak öğrencilerin başarı puanlarını tahmin etmeyi amaçlamaktadır. Bu kapsamda iki farklı doğrusal regresyon yöntemi uygulanmıştır:

- **Kapalı Form (WLSE)** yöntemi
- **Gradient Descent (GD)** yöntemi

Her iki yaklaşım da Python dilinde ve NumPy, Pandas, Matplotlib gibi kütüphaneler kullanılarak gerçekleştirilmiştir.

---

## 🧪 Uygulanan Modeller

### 1️⃣ WLSE (With Least Squares Estimation)
- Kullanılan dosya: `LinearRegressionWLSE.ipynb`
- Yöntem: \( \theta = (X^T X)^{-1} X^T y \) kapalı form çözüm
- Model Scikit-learn ile karşılaştırılarak doğrulandı.
- Kullanılan metrik: **Mean Squared Error (MSE)**
- Grafik: Gerçek vs Tahmin görselleştirmesi mevcut

### 2️⃣ Gradient Descent ile Regresyon
- Kullanılan dosya: `LinearRegressionWSLearn.ipynb`
- Veriler z-score normalizasyonu ile standardize edildi.
- Aşamalar:
  - Bias (sabit) terimi eklendi
  - Cost fonksiyonu tanımlandı
  - Parametre güncellemeleri yapıldı
- Grafikler:
  - Maliyet fonksiyonunun iterasyonlara göre değişimi
  - Gerçek vs Tahmin edilen değerler karşılaştırması

---

## 🔍 Sonuç Karşılaştırması

| Özellik           | WLSE                         | Gradient Descent                |
|------------------|------------------------------|----------------------------------|
| Model Türü        | Kapalı Form (Analitik)        | Sayısal Optimizasyon             |
| Ölçekleme         | Gerekli değil                | Z-score normalization yapıldı    |
| Hata Metrikleri   | MSE                          | MSE                              |
| Performans        | Hızlı ve doğrudan çözüm      | Daha esnek, büyük veri için uygun |
| Görseller         | Gerçek vs Tahmin            | Cost eğrisi + Tahmin Grafiği     |

---

## 📁 Klasör ve Dosyalar

- `LinearRegressionWLSE.ipynb`: WLSE yöntemiyle tahmin
- `LinearRegressionWSLearn.ipynb`: GD yöntemiyle tahmin
- `student-performance.csv`: Kullanılan veri seti (indirme bağlantısı yoksa eklenecek)

---

## 🏁 Sonuç

Bu çalışmada iki farklı regresyon yöntemi uygulanmış ve performansları karşılaştırılmıştır. WLSE yöntemi küçük veri kümelerinde daha hızlı sonuç verirken, GD yöntemi daha büyük ve karmaşık veri kümelerinde uyarlanabilirlik açısından avantajlıdır.

---

## 🔗 Kaynaklar

- [Student Performance Dataset - Kaggle](https://www.kaggle.com/datasets/jessemostipak/student-performance)
- [NumPy Linear Algebra Docs](https://numpy.org/doc/stable/reference/routines.linalg.html)
- [Gradient Descent Optimization](https://towardsdatascience.com/linear-regression-using-gradient-descent-97a6c8700931)
