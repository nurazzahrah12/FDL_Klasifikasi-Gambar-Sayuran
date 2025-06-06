# Proyek Klasifikasi Gambar: Sayuran

## Deskripsi Proyek
Proyek ini bertujuan membangun model klasifikasi gambar menggunakan Convolutional Neural Network (CNN) untuk mendeteksi jenis sayuran dari gambar. Dataset yang digunakan berisi lebih dari 10.000 gambar yang terbagi dalam 15 kelas berbeda. Proyek ini berhasil mencapai akurasi lebih dari 98% di training dan test set, memenuhi seluruh kriteria evaluasi yang ditetapkan.

## Struktur Folder

```
.
├── cnn_baseline_model.h5   
├── model.keras           
├── saved_model/                 
├── tfjs_model/                  
├── tflite/                      
├── Kriteria Submission.txt     
├── requirements.txt             
├── README.md                    
├── submission-klasifikasi-gambar-nur-salamah-azzahrah.ipynb
```

## Pencapaian

- Dataset berisi >10.000 gambar dengan 15 kelas berbeda
- Akurasi training & testing set di atas 98%
- Model diekspor ke dalam 3 format: SavedModel, TF-Lite, dan TFJS
- Visualisasi akurasi dan loss
- Arsitektur CNN menggunakan Conv2D, Pooling, Flatten, Dense
- Inference dilakukan dengan model yang telah disimpan

## Tahapan Proyek

### 1. Preprocessing & Augmentasi
- Resize ke 224x224
- Normalisasi piksel ke [0, 1]
- Augmentasi: rotasi, flip, zoom, dsb.

### 2. Arsitektur CNN
Menggunakan Keras `Sequential`:
- Conv2D, MaxPooling2D, Flatten, Dense
- Callbacks: EarlyStopping, ReduceLROnPlateau

### 3. Evaluasi
- Plot akurasi dan loss (training vs validation)
- Confusion matrix, classification report
- Akurasi mencapai >98%

### 4. Export Model
Model disimpan ke:
- `saved_model/`
- `tflite/`
- `tfjs_model/`
- `cnn_baseline_model.h5`, `model.keras`

*Semua file besar ini tidak disertakan dalam repository GitHub karena keterbatasan ukuran.*

## Cara Menjalankan Proyek

1. Install dependensi:
   ```bash
   pip install -r requirements.txt
   ```

2. Jalankan notebook:
   - `submission-klasifikasi-gambar-nur-salamah-azzahrah.ipynb`

3. Untuk inference, gunakan gambar input berukuran 224x224

## Saran Pengembangan

- Gunakan dataset dengan resolusi gambar yang tidak seragam
- Tambahkan cross-validation dan hyperparameter tuning
- Eksplorasi model pre-trained (transfer learning)
- Dokumentasikan setiap fungsi dan tahap
- Jaga struktur dan kebersihan kode
