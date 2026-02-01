# Customer Segmentation with K-Means Clustering

Bu proje, bir müşteri veri kümesini kullanarak benzer harcama alışkanlıklarına
ve gelir düzeylerine sahip müşteri gruplarını belirlemek amacıyla geliştirilmiş bir **Gözetimsiz Öğrenme (Unsupervised Learning)** çalışmasıdır.

Proje Özeti
Müşteri verileri (Gelir ve Harcama Skoru), makine öğrenmesi süreçlerinden geçirilerek analiz edilmiş ve **K-Means Algoritması** ile anlamlı segmentlere ayrılmıştır.
Bu tür analizler, işletmelerin hedef kitlelerine özel pazarlama stratejileri geliştirmesine yardımcı olur.


## 🛠️ Uygulanan Adımlar

1. **Veri Temizleme:** Analiz için gerekli olmayan 'Gender', 'Profession', 'Age' gibi sütunlar kaldırılarak odak noktası 'Income' ve 'Score' olarak belirlendi.
2. **Ölçeklendirme (Scaling):** Gelir ve skor değerleri arasındaki büyük farkları dengelemek için `MinMaxScaler` kullanılarak veriler 0-1 arasına normalize edildi.
3. **Elbow Method (Dirsek Metodu):** Veri kümesi için en ideal küme sayısı (K değeri), WCSS (Inertia) değerleri hesaplanarak belirlendi.
4. **Modelleme:** Belirlenen ideal küme sayısı (K=4) ile K-Means modeli eğitildi ve müşteriler segmente edildi.
5. **Görselleştirme:** Küme merkezleri (centroids) ve segmentler renkli dağılım grafiği (scatter plot) üzerinde gösterildi.

Sonuçlar
Model sonucunda müşteriler 4 ana gruba ayrılmıştır:
- **Grup 0:** (Örn: Düşük Gelir - Düşük Harcama)
- **Grup 1:** (Örn: Yüksek Gelir - Yüksek Harcama)
- **Grup 2:** ...
- **Grup 3:** ...

> *Not: Küme merkezleri grafikte mavi 'X' işareti ile belirtilmiştir.*
> 
![Müşteri Segmentasyonu](musteri_segmentasyonu.png)
