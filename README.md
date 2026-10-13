# Undams-ID

Aplikasi web berbasis Flask untuk mengidentifikasi tanaman obat dari gambar menggunakan model TensorFlow/Keras. Model mengenali empat kelas: **Lengkuas**, **Temulawak**, **Kunyit**, dan **Jahe**.

## Persyaratan

- Python 3.9 atau lebih baru
- File model `model_new3.h5` di direktori utama proyek

## Menjalankan aplikasi

Buka PowerShell di direktori proyek, lalu buat dan aktifkan virtual environment:

```powershell
py -m venv myenv
.\myenv\Scripts\Activate.ps1
```

Pasang dependensi yang digunakan aplikasi:

```powershell
python -m pip install Flask numpy tensorflow requests Pillow gradio
```

Jalankan aplikasi:

```powershell
python app.py
```

Buka [http://localhost:5000](http://localhost:5000) di browser. Pilih gambar tanaman, lalu tekan tombol **Identification** untuk melihat hasil prediksi.

## Struktur proyek

```text
.
├── app.py                  # Aplikasi Flask dan proses prediksi
├── model_new3.h5           # Model klasifikasi Keras
├── static/                 # CSS, JavaScript, gambar, dan aset tampilan
└── templates/              # Halaman HTML Flask
```

Gambar yang diunggah untuk prediksi disimpan di `static/img/predict_img/`. Isi folder tersebut diabaikan oleh Git.

## Catatan

- Pastikan `model_new3.h5` tersedia di direktori utama sebelum menjalankan aplikasi.
- Aplikasi saat ini dijalankan dengan mode debug Flask dan ditujukan untuk penggunaan lokal. Untuk deployment, gunakan server WSGI dan nonaktifkan mode debug.
