# BLM0463 Veri Madenciliğine Giriş — Dönem Projesi

KNN (K-Nearest Neighbors) ile **UCI Vertebral Column** veri seti üzerinde sınıflandırma.

## Öğrenci Bilgileri
- **Ad-Soyad:** Eren Bezek
- **Numara:** 22360859011
- **Ders:** BLM0463 Veri Madenciliğine Giriş
- **Yöntem:** K-Nearest Neighbors
- **Veri Seti:** [Vertebral Column — UCI ML Repository (ID 212)](https://archive.ics.uci.edu/dataset/212/vertebral+column)

## Veri Seti
- 310 hasta, 6 biyomekanik özellik:
  1. `pelvic_incidence` — Pelvik İnsidans
  2. `pelvic_tilt` — Pelvik Eğim
  3. `lumbar_lordosis_angle` — Lumbar Lordosis Açısı
  4. `sacral_slope` — Sakral Eğim
  5. `pelvic_radius` — Pelvik Yarıçap
  6. `degree_spondylolisthesis` — Spondilolistezis Derecesi
- İki etiket sürümü:
  - **2-sınıflı:** Normal (100) / Abnormal (210)
  - **3-sınıflı:** Normal (100) / Hernia (60) / Spondylolisthesis (150)

## Klasör Yapısı
```
.
├── BLM463_Proje_KNN.ipynb        # Ana Jupyter Notebook
├── data/
│   ├── column_2C_weka.csv         # UCI'dan indirilen veri (2-sınıflı)
│   └── column_3C_weka.csv         # UCI'dan indirilen veri (3-sınıflı)
├── figures/                       # Üretilen grafikler ve tablolar
├── requirements.txt
└── README.md
```

## Kurulum ve Çalıştırma
```bash
pip install -r requirements.txt
jupyter notebook BLM463_Proje_KNN.ipynb
```

## Pipeline Özeti
1. EDA — eksik değer kontrolü, özet istatistik, sınıf dengesi
2. Görselleştirme — countplot, korelasyon heatmap, boxplot, pairplot
3. Önişleme — `StandardScaler` ile normalize, %80/%20 stratified split
4. Modelleme — KNN
5. Hiperparametre seçimi — `k` için 1-30 arası 10-katlı CV taraması
6. Mesafe metriği karşılaştırması — euclidean, manhattan, chebyshev, minkowski
7. Değerlendirme — Accuracy, Precision, Recall, F1, Specificity, Confusion Matrix, ROC-AUC
8. Literatür karşılaştırması

## Sonuç Videosu
[YouTube linki buraya eklenecek]

## Lisans
Akademik proje. Veri seti UCI Machine Learning Repository'den alınmıştır.
