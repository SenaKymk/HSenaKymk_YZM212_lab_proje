Özdeğerler, Özvektörler ve Makine Öğrenmesindeki Rolü

🔹 Kavramsal Tanımlar

Özvektör (Eigenvector): Bir matrisle çarpıldığında sadece skaler bir katsayı (lambda) kadar yönü değişmeyen vektörlerdir.

Özdeğer (Eigenvalue): Bu skaler katsayının kendisidir. Özvektöre karşılık gelen çarpan değeridir.

 Matematiksel ifade:

Burada  kare matris,  bir özvektör,  ise karşılık gelen özdeğerdir.

 Makine Öğrenmesindeki Kullanım Alanları

1.  Principal Component Analysis (PCA)

Boyut indirgeme tekniğidir.

Kovaryans matrisinin özvektörleri, verinin en çok bilgi taşıyan yönleridir.

Özdeğerler, her özvektörün verideki varyansa katkısını belirtir.

 → kovaryans matrisi

2.  Singular Value Decomposition (SVD)

Özellikle görüntü işleme ve metin madenciliği gibi alanlarda kullanılır.

Herhangi bir  matrisi:



şeklinde ayrıştırılabilir. Bu ayrıştırma, verinin önemli özelliklerini tutan bileşenleri çıkarır.

3.  Google PageRank

Web sayfaları arasındaki bağlantılar bir olasılık matrisi olarak tanımlanır.

Bu matrisin dominant özvektörü, sayfaların "önem derecesini" belirler.

4.  Spektral Kümeleme (Spectral Clustering)

Benzerlik matrisi oluşturulur.

Bu matrisin özvektörleri kullanılarak veri görsel olarak ayrıştırılır.

 Teorik Arka Plan

Özdeğer denkleminden karakteristik denklem çıkarılmış:


Determinant şartı:

 çözülerek özdeğerler hesaplanır.

Eigen decomposition:



Simetrik matrisler için:



SVD ve boyut indirgeme uygulaması el yazısıyla çizilmiş.
