# 🍷 Wine Quality Classification

Proyek ini merupakan implementasi model klasifikasi untuk memprediksi kualitas anggur berdasarkan fitur-fitur kimiawi menggunakan algoritma **Random Forest Classifier**.

---

## Dataset

Dataset yang digunakan adalah **Wine Quality Dataset** yang terdiri dari dua file:

| File | Keterangan |
|------|-----------|
| `data_training.csv` | 857 sampel dengan label `quality` |
| `data_testing.csv` | 286 sampel tanpa label (data prediksi) |

Variabel target adalah `quality` dengan skala 0–10. Terdapat 11 fitur kimiawi sebagai prediktor, antara lain `alcohol`, `volatile acidity`, `sulphates`, `citric acid`, dan lainnya.

---

## Alur Notebook

**1. Import Library** — Memuat seluruh library yang dibutuhkan (pandas, sklearn, matplotlib, seaborn).

**2. Load Dataset** — Membaca data training dan testing dari file CSV.

**3. Eksplorasi Data (EDA)** — Analisis distribusi target, pengecekan missing value, heatmap korelasi, dan boxplot fitur terhadap kualitas.

**4. Persiapan Data** — Memisahkan fitur dan variabel target.

**5. Pemodelan** — Melatih Random Forest Classifier dengan 300 estimator dan `max_features='sqrt'`.

**6. Evaluasi** — Mengukur performa model menggunakan Cross-Validation 5-Fold, Classification Report, dan Confusion Matrix.

**7. Prediksi Final** — Model dilatih ulang dengan seluruh data training, kemudian digunakan untuk memprediksi data testing.

**8. Simpan Hasil** — Hasil prediksi disimpan dalam `submission.csv` yang hanya memuat kolom `id` dan `quality`.

---

## Hasil Evaluasi

| Metric | Nilai |
|--------|-------|
| CV Accuracy (5-Fold) | ~64.30% |
| Fitur Terpenting | alcohol, sulphates, volatile acidity |
| Total Prediksi | 286 sampel |

Akurasi ~64% merupakan hasil yang wajar mengingat dataset Wine Quality bersifat imbalanced — mayoritas sampel terkonsentrasi pada kelas 5 dan 6.

---

## Output

File `submission.csv` berisi hasil prediksi dengan format:

```
id,quality
222,5
1514,6
...
```

---

## Tools & Library

Python 3 · pandas · scikit-learn · matplotlib · seaborn
