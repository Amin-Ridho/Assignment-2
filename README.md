# Assignment 02 machine learning & deep learning

02_KELOMPOK D_1 Klasifikasi dengan Model Pembelajaran Mesin Terbimbing

Kumpulan data : SC_HW1_bank_data
Perpustakaan : Pandas, Numpy, Scikit-learn
Tujuan : Membangun model klasifikasi untuk memprediksi kolom target “Exited”.
Langkah-langkah :

Menghapus Kolom Tidak Relevan : Hilangkan kolom yang tidak diperlukan untuk mencetak agar data lebih bersih.
One-Hot Encoding : Lakukan pengkodean one-hot menggunakan pd.get_dummies()untuk kategorikal data.
Pisahkan Fitur (X) dan Target (Y) : Pisahkan variabel fitur (X) dan target (Y), di mana Y merujuk ke kolom "Exited".
Scaling atau Normalisasi : Lakukan scaling untuk memastikan data berada dalam rentang yang sesuai.
Model yang dipilih :

Model #1 : Regresi Logistik. Model ini dipilih karena sederhana dan cocok untuk klasifikasi biner.
Model #2 : Pohon Keputusan. Model ini menawarkan interpretasi yang jelas melalui pohon keputusan dan sering kali berguna untuk data dengan fitur yang kompleks.
Model #3 : Hutan Acak. Merupakan ansambel dari banyak pohon keputusan yang meningkatkan akurasi dengan mengurangi risiko overfitting.
valuasi : Setiap model dievaluasi berdasarkan akurasi dan laporan klasifikasi. Model terbaik dipilih dengan mempertimbangkan metrik seperti akurasi, presisi, recall, dan f1-score.

02_KELOMPOK D_2 Segmentasi Data dengan Clustering KMeans

Kumpulan data : cluster_s1
Pustaka : Pandas, Numpy, Scikit-learn, Matplotlib, Seaborn
Tujuan : Mengelompokkan data menjadi beberapa cluster menggunakan KMeans.
Langkah-langkah :

Menentukan Jumlah Cluster Terbaik : Gunakan Metode Elbow atau Silhouette Score untuk menemukan jumlah cluster yang optimal.
Pemodelan dengan KMeans : Bangun model KMeans dengan jumlah cluster yang telah ditentukan.
Masukkan Label Cluster ke dalam DataFrame : Tambahkan kolom label hasil clustering ke DataFrame untuk mengetahui cluster dari tiap data.
Plot Hasil Clustering : Visualisasikan hasil clustering dengan Seaborn untuk melihat pembagian data dalam setiap cluster.
Dengan langkah-langkah ini, Anda dapat melakukan segmentasi data menggunakan KMeans dan memvisualisasikan hasilnya untuk analisis lebih lanjut.

02_KELOMPOK D_3 Regresi dengan TensorFlow-Keras

Tugas : Memprediksi Harga Rumah
Dataset : Harga Rumah di California
Tujuan : Melakukan prediksi harga rumah dengan pengaturan input ganda menggunakan Multilayer Perceptron (MLP).
langkah-langkah :

Mengonversi Data ke DataFrame : Ubah array numpy featuresdan targetke bentuk Pandas DataFrame untuk kemudahan manipulasi data.
Membagi Data : Pisahkan data menjadi train, validation, dan test untuk melatih dan menguji performa model.
Standarisasi dan Normalisasi : Standarisasi menggunakan StandardScalerdan normalisasi dengan MinMaxScalerdata train, validation, dan test.
Membangun Model :
Buat lapisan tersembunyi pertama dengan 30 neuron dan fungsi aktivasi ReLU.
Buat layer tersembunyi kedua dengan 30 neuron dan fungsi aktivasi ReLU.
Pengaturan Pelatihan : Tentukan jumlah epoch (jumlah iterasi pelatihan). Tentukan ukuran batch.
Simpan dan Muat Ulang Model : Tentukan nama file dengan ekstensi kerasuntuk menyimpan model, kemudian muat ulang model untuk prediksi dengan data baru ( x_new_Adan x_new_B).

02_KELOMPOK D_4 Klasifikasi dengan PyTorch

Tugas : Mengklasifikasikan Transaksi Penipuan Kartu Kredit
Dataset : Penipuan Kartu Kredit 2023
Tujuan : Klasifikasi transaksi penipuan kredit menggunakan Multilayer Perceptron (MLP) dengan framework PyTorch.
Langkah-langkah :

Mengimpor Dataset : Gunakan fungsi read_by_CPUuntuk mengimpor dataset ke dalam Pandas DataFrame.
Menghapus Kolom ID : Hilangkan kolom ID agar tidak mengubah klasifikasi.
Menentukan Fitur dan Target : Gunakan data_gpuuntuk mendefinisikan X (fitur) dan Y (target).
Membagi Dataset :
Gunakan splitCPUuntuk membagi dataset dengan komposisi 80% untuk train set dan 20% untuk test set.
Gunakan splitGPUuntuk membagi dataset yang sama pada GPU.
Aktifkan GPU : Gunakan CUDA untuk mempercepat proses pelatihan.
Pengaturan Batch dan Hyperparameter :
Tentukan ukuran batch dan atur model hyperparameter seperti jumlah epoch, learning rate, dll.
Parameter dan Hyperparameter :
Parameter : Nilai model yang dipelajari selama pelatihan (misalnya, bobot dan bias neuron).
Hyperparameters : Pengaturan yang menentukan bagaimana model dibor, seperti jumlah epoch, learning rate, atau ukuran batch.
Input Model dan Parameter yang Dapat Dilatih :
entukan ukuran input sesuai dengan fitur pada data.
Semua parameter pada MLP bersifat "trainable", sehingga total parameter sama dengan parameter yang dapat dibor.
ine-Tuning : Jika akurasi model masih di bawah 95%, lakukan fine-tuning engan mengatur kembali hyperparameters atau menambah lapisan dan neuron pada model.
