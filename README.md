## 📂 Struktur & Tahapan Proyek

1. **Eksplorasi & Pembersihan Data (Data Exploration):**
   * Menggunakan dua dataset historis saham: **AAPL.csv** (Apple Inc.) dan **AMD.csv** (Advanced Micro Devices).
   * Pengecekan nilai kosong (*missing values*), duplikasi data, serta analisis statistik deskriptif dari rentang tahun 1980 hingga 2020.
   * Analisis korelasi fitur (*feature correlation matrix*) untuk pemilihan fitur yang paling optimal (memilih fitur `Close` untuk menghindari multikolinearitas yang tinggi pada fitur harga lainnya).

2. **Persiapan Data Time Series (Windowing & Splitting):**
   * Pemisahan data input dan output menggunakan **Window Size = 5** dan **Horizon = 1**.
   * Pembagian data latih dan validasi dengan proporsi **90% Train Set** dan **10% Validation Set**.

3. **Pembangunan dan Pelatihan Model (Deep Learning - LSTM):**
   * Membangun arsitektur model menggunakan TensorFlow/Keras (Sequential, LSTM, Dropout, BatchNormalization, Dense).
   * Penerapan *callbacks* seperti `EarlyStopping` dan `ReduceLROnPlateau` untuk mengoptimalkan proses pelatihan (*training*) serta mencegah *overfitting*.
   * Evaluasi model menggunakan metrik kesalahan seperti *Mean Squared Error* (MSE) dan *Mean Absolute Error* (MAE).

---

## 🛠️ Kebutuhan Sistem & Instalasi

Pastikan Anda telah memasang pustaka berikut sebelum menjalankan notebook:

```bash
pip install statsmodels -q
