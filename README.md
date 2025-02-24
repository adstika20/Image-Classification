# Prediksi dan Klasifikasi Penyakit Tanaman Kentang Menggunakan Densnet 🍂

# Deskripsi Proyek
Proyek ini bertujuan untuk mendeteksi dan mengklasifikasikan kondisi tanaman kentang berdasarkan gambar daun, mengidentifikasi apakah tanaman mengalami penyakit early blight, late blight, atau dalam kondisi sehat. Model ini dilatih menggunakan dataset yang terdiri dari 1.722 gambar untuk training, 430 gambar untuk validasi, dan 2.152 gambar untuk pengujian, dengan tiga kategori label utama, yaitu Potato___Early_blight (0), Potato___Late_blight (1), dan Potato___healthy (2).

Model dikembangkan menggunakan arsitektur DenseNet121 sebagai backbone dengan bobot awal dari ImageNet, yang tidak dilatih ulang pada tahap awal untuk mempertahankan fitur-fitur pretrained. Setelah backbone, model dilengkapi dengan beberapa lapisan tambahan, termasuk normalisasi batch, lapisan fully connected dengan aktivasi ReLU, dropout untuk mengurangi overfitting, dan lapisan output dengan tiga neuron menggunakan aktivasi softmax. Model ini dirancang untuk mengoptimalkan kinerja klasifikasi dengan memanfaatkan kombinasi feature extraction dari DenseNet dan lapisan tambahan yang lebih dalam untuk meningkatkan akurasi dalam mendeteksi penyakit pada tanaman kentang.

# Cara Instalasi
Sebelum menjalankan proyek ini, pastikan Anda memiliki Python dan semua dependensi yang diperlukan. Anda dapat menginstalnya dengan menggunakan file requirements.txt yang telah disediakan.
1. Pastikan Python telah terinstal
Proyek ini berjalan dengan Python 3.7 atau versi lebih tinggi. Anda dapat mengecek versi Python dengan perintah berikut:
```
python --version
```
2. Buat virtual environment (Opsional, tetapi disarankan)
Disarankan menggunakan virtual environment agar tidak mengganggu sistem utama. Jalankan perintah berikut untuk membuat dan mengaktifkan environment baru:
```
python -m venv env
source env/bin/activate  # Untuk pengguna macOS/Linux
env\Scripts\activate     # Untuk pengguna Windows
```
3. Instal dependensi proyek
Setelah virtual environment aktif, instal semua dependensi dengan perintah berikut:
```
pip install -r requirements.txt
```
5. Verifikasi Instalasi
Untuk memastikan semua dependensi telah terinstal dengan benar, jalankan:
```
python -c "import tensorflow as tf; print(tf.__version__)"
```

# Hasil

Model dilatih selama 20 epoch dengan hasil yang menunjukkan kinerja yang sangat baik dalam mengklasifikasikan kondisi tanaman kentang. Pada akhir pelatihan, model mencapai akurasi sebesar 99,05% dengan nilai loss sebesar 0,0573. Saat diuji menggunakan dataset pengujian, model tetap menunjukkan performa tinggi dengan nilai test loss sebesar 0,0534 dan test accuracy sebesar 98,70%. Hasil ini menunjukkan bahwa model memiliki kemampuan generalisasi yang sangat baik dalam mengenali pola dan fitur penyakit pada daun kentang, sehingga dapat digunakan sebagai alat bantu yang andal dalam diagnosis penyakit tanaman secara otomatis.


# Sumber Data 
[Kaggle](https://www.kaggle.com/datasets/hafiznouman786/potato-plant-diseases-data/data)
