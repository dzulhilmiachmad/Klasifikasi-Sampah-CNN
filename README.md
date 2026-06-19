# Klasifikasi-Sampah-CNN
File ini berisi dokumen-dokumen yang dibutuhkan untuk tugas proyek UAS mata kuliah kecerdasan buatan

# Klasifikasi Sampah Menggunakan Convolutional Neural Network (CNN)
Deskripsi Proyek
Proyek ini merupakan tugas pengganti UAS Mata Kuliah Kecerdasan Buatan pada Program Studi Teknik Elektro.

Tujuan proyek ini adalah membangun sistem klasifikasi sampah berbasis kecerdasan buatan menggunakan metode Convolutional Neural Network (CNN). 
Sistem dapat mengenali jenis sampah berdasarkan citra yang diberikan dan mengelompokkannya ke dalam kategori yang sesuai.

# Dataset
Dataset yang digunakan adalah TrashNet Dataset yang berisi gambar berbagai jenis sampah.
https://www.kaggle.com/datasets/feyzazkefe/trashnet

# Kategori Kelas
Cardboard (Kardus)
Glass (Kaca)
Metal (Logam)
Paper (Kertas)
Plastic (Plastik)
Trash (Sampah Lainnya)

Jumlah dataset yang digunakan sekitar 2527 gambar.

# Struktur dataset:
dataset-resized/
├── cardboard/
├── glass/
├── metal/
├── paper/
├── plastic/
└── trash/

# Tahapan Pengerjaan
1. Preprocessing Data
   Tahapan preprocessing yang dilakukan:
   Resize gambar menjadi 128 × 128 piksel
   Normalisasi nilai piksel dari 0–255 menjadi 0–1
   Pembagian dataset:
   80% data training
   20% data validation
2. Pembuatan Model CNN
   Arsitektur CNN yang digunakan:
   Conv2D (16 filter)
   MaxPooling2D
   Conv2D (32 filter)
   MaxPooling2D
   Flatten
   Dense (64 neuron)
   Dense Output (6 kelas dengan Softmax)
3. Training Model
   Konfigurasi training:
   Optimizer: Adam
   Loss Function: Categorical Crossentropy
   Batch Size: 32
   Epoch: 10

# Hasil Pengujian
Akurasi Model
Training Accuracy: 99,06%
Validation Accuracy: 50,89%

# Classification Report
Kelas	        Precision	Recall	F1-Score
Cardboard	    0.58	    0.41	  0.48
Glass	        0.46	    0.62	  0.53
Metal	        0.39	    0.39	  0.39
Paper	        0.69	    0.78	  0.73
Plastic	      0.37	    0.24	  0.29
Trash	        0.42	    0.52	  0.47

Akurasi validasi keseluruhan mencapai sekitar 51%.

# Analisis Hasil
Berdasarkan hasil pelatihan, model memperoleh akurasi training yang sangat tinggi yaitu 99,06%, sedangkan akurasi validation sebesar 50,89%.
Perbedaan yang cukup besar antara kedua nilai tersebut menunjukkan bahwa model mengalami overfitting, yaitu model mampu mengenali data trai-
ning dengan sangat baik tetapi kemampuan generalisasi terhadap data baru masih terbatas. Kelas dengan performa terbaik adalah Paper dengan 
nilai F1-Score sebesar 0,73, sedangkan kelas Plastic memiliki performa terendah dengan nilai F1-Score sebesar 0,29.

# Struktur Proyek
Klasifikasi-Sampah-CNN/
│
├── CNN_Klasifikasi_Sampah.ipynb
├── cnn_sampah.keras
├── README.md
├── accuracy_graph.png
├── loss_graph.png
├── confusion_matrix.png
└── dataset/

# Cara Menjalankan Program
- Buka Google Colab.
- Upload file notebook (.ipynb).
- Hubungkan Google Drive.
- Pastikan dataset berada pada folder yang sesuai.
- Jalankan seluruh sel secara berurutan.
- Upload gambar baru untuk melakukan prediksi.

# Hasil Demo
Model berhasil melakukan prediksi terhadap gambar uji baru dan dapat mengenali:
- Sampah plastik (Plastic)
- Sampah kardus (Cardboard)
- Sampah besi (Metal)
- Sampah bungkus (Trash)
- Sampah kaca (Glass)
- Sampah kertas (Paper)

# Kesimpulan
Pada proyek ini berhasil dibangun sistem klasifikasi sampah berbasis Convolutional Neural Network (CNN) menggunakan dataset TrashNet. 
Model mampu mengklasifikasikan gambar ke dalam enam kategori sampah dengan akurasi validasi sekitar 51%, Meskipun masih terdapat ind-
ikasi overfitting, hasil yang diperoleh menunjukkan bahwa metode CNN dapat digunakan untuk membantu proses klasifikasi sampah secara 
otomatis berdasarkan citra.

Penulis

Achmad Dzulhilmi
235060301111016
Program Studi Teknik Elektro
Mata Kuliah Kecerdasan Buatan / Kelas C
