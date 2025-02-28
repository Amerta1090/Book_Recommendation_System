# Laporan Proyek Machine Learning - Abdul Majid Ridwan Tyastonoatmaja
## Project Overview

### Latar Belakang

Di era digital saat ini, jumlah buku yang tersedia di pasaran semakin meningkat, yang membuat pembaca kesulitan menemukan buku yang sesuai dengan minat dan preferensi mereka. Sistem rekomendasi buku adalah solusi yang efektif untuk membantu pengguna menemukan buku yang relevan berdasarkan preferensi mereka[^1]. Proyek ini bertujuan untuk mengembangkan sistem rekomendasi buku menggunakan dua pendekatan utama: Content-Based Filtering dan Collaborative Filtering[^1].

Sistem rekomendasi yang efektif tidak hanya meningkatkan pengalaman pengguna tetapi juga dapat meningkatkan penjualan buku dan kepuasan pelanggan[^1]. Tujuan utama dari sistem rekomendasi buku adalah membantu pembaca menemukan buku yang sesuai dengan minat, preferensi, atau riwayat bacaan mereka[^1]. Hal ini dapat meningkatkan kepuasan pelanggan dan membantu mereka menemukan buku yang mungkin mereka nikmati tetapi sebelumnya tidak mereka sadari[^1].

### Pentingnya Proyek Ini

Proyek ini penting untuk diselesaikan karena:

* **Meningkatkan Pengalaman Pengguna**: Dengan sistem rekomendasi yang efektif, pengguna dapat dengan mudah menemukan buku yang sesuai dengan minat mereka, menghemat waktu dan usaha dalam pencarian[^1].
* **Meningkatkan Penjualan**: Rekomendasi yang akurat dapat meningkatkan penjualan buku karena pengguna lebih cenderung membeli buku yang direkomendasikan berdasarkan preferensi mereka[^1].
* **Analisis Data**: Proyek ini juga memberikan wawasan tentang preferensi pembaca dan tren di industri buku, yang dapat digunakan oleh penerbit dan penulis untuk mengembangkan konten yang lebih sesuai dengan kebutuhan pasar[^5]. Dengan memanfaatkan data pengguna dan buku, sistem ini dapat memberikan rekomendasi yang lebih personal dan relevan, sehingga membantu pengguna membuat keputusan pembelian yang lebih baik[^1].

### Referensi

* BISA AI. Portofolio :: Sistem Rekomendasi Buku. [https://bisa.ai/portofolio/detail/MzM4OQ](https://bisa.ai/portofolio/detail/MzM4OQ)[^1]
* Ritdrix, Andrew Hans, dan Panji Wisnu Wirawan. "Sistem Rekomendasi Buku Menggunakan Metode Item-Based Collaborative Filtering." *Jurnal Masyarakat Informatika*, vol. 9, no. 2, 2018, hal. 24-31. [http://download.garuda.kemdikbud.go.id/article.php?article=1748276\&val=1291\&title=Sistem+Rekomendasi+Buku+Menggunakan+Metode+Item-Based+Collaborative+Filtering](http://download.garuda.kemdikbud.go.id/article.php?article=1748276&val=1291&title=Sistem+Rekomendasi+Buku+Menggunakan+Metode+Item-Based+Collaborative+Filtering)[^3]
* Fathurrahman, Mohammad Iqbal, Dade Nurjanah, dan Rita Rismala. "Sistem Rekomendasi Buku Menggunakan Metode Trust-Aware Recommendation." *School of Computing, Telkom University*, 2019. [https://core.ac.uk/download/pdf/299917962.pdf](https://core.ac.uk/download/pdf/299917962.pdf)[^9]
* Safitri, Asa Dilla, Vihi Atina, dan Anisatul Farida. "Sistem Rekomendasi Buku Menggunakan Metode Content-Based Filtering." *Jurnal Infotech*, vol. 9, no. 1, 2024, hal. 60-67. [https://jurnal.sttmcileungsi.ac.id/index.php/infotech/article/view/1302](https://jurnal.sttmcileungsi.ac.id/index.php/infotech/article/view/1302)[^7]
* Sutikno, T., dkk. "Sistem Rekomendasi Buku di Perpustakaan Daerah Jepara Menggunakan Metode Item-Based Collaborative Filtering." *BINER : Jurnal Ilmiah Aplikasi Teknologi Informasi*, vol. 1, no. 2, 2023, hal. 83-90. [https://ojs.unsiq.ac.id/index.php/biner/article/view/3934](https://ojs.unsiq.ac.id/index.php/biner/article/view/3934)[^5]

[^1]: https://bisa.ai/portofolio/detail/MzM4OQ

[^2]: https://lib.ub.ac.id/berita/budaya-membaca-di-era-gadget-strategi-menghadapi-tantangan/

[^3]: http://download.garuda.kemdikbud.go.id/article.php?article=1748276\&val=1291\&title=Sistem+Rekomendasi+Buku+Menggunakan+Metode+Item-Based+Collaborative+Filtering

[^4]: https://static.buku.kemdikbud.go.id/content/pdf/bukuteks/kurikulum21/Dasar-Pengembangan-Perangkat-Lunak-dan-Gim-BS-KLS-X.pdf

[^5]: https://ojs.unsiq.ac.id/index.php/biner/article/view/3934

[^6]: https://eprints.umpo.ac.id/13675/3/3. BAB I.pdf

[^7]: https://jurnal.sttmcileungsi.ac.id/index.php/infotech/article/view/1302

[^8]: https://crmsindonesia.org/wp-content/uploads/2020/09/Buku-Kumpulan-Studi-Kasus-Manajemen-Risiko-di-Indonesia.pdf

[^9]: https://core.ac.uk/download/pdf/299917962.pdf

---

## Business Understanding

### Problem Statements

- **Pernyataan Masalah 1**:  
  Ketersediaan buku yang sangat banyak membuat pengguna kesulitan menemukan buku yang sesuai dengan preferensi mereka. Hal ini dapat mengurangi pengalaman pengguna dalam menemukan buku yang relevan.

- **Pernyataan Masalah 2**:  
  Data rating buku yang diberikan oleh pengguna seringkali tidak merata, dengan beberapa buku mendapatkan banyak rating sementara yang lain hanya mendapatkan sedikit atau bahkan tidak ada rating sama sekali. Hal ini menyulitkan sistem untuk memberikan rekomendasi yang akurat.

- **Pernyataan Masalah 3**:  
  Pengguna baru atau pengguna yang jarang memberikan rating (cold start problem) sulit mendapatkan rekomendasi yang sesuai karena kurangnya data historis tentang preferensi mereka.

### Goals

- **Jawaban Pernyataan Masalah 1**:  
  Membangun sistem rekomendasi yang dapat membantu pengguna menemukan buku yang sesuai dengan preferensi mereka berdasarkan data historis rating dan informasi buku.

- **Jawaban Pernyataan Masalah 2**:  
  Mengembangkan model yang dapat mengatasi ketidakmerataan data rating dengan memfilter buku dan pengguna yang memiliki terlalu sedikit rating, sehingga meningkatkan akurasi rekomendasi.

- **Jawaban Pernyataan Masalah 3**:  
  Menerapkan pendekatan yang dapat memberikan rekomendasi yang relevan bahkan untuk pengguna baru atau pengguna dengan sedikit data rating, seperti menggunakan pendekatan content-based filtering.

### Solution Approach

### Solution Statements

- **Solution Approach 1: Content-Based Filtering**  
  - **Deskripsi**:  
    Pendekatan ini merekomendasikan buku berdasarkan kesamaan konten atau fitur buku, seperti penulis, penerbit, dan tahun terbit. Dengan menggunakan teknik TF-IDF dan cosine similarity, sistem dapat menemukan buku yang mirip dengan buku yang telah disukai oleh pengguna sebelumnya.  
  - **Keuntungan**:  
    Cocok untuk mengatasi masalah cold start karena tidak memerlukan data rating dari pengguna lain.  
  - **Implementasi**:  
    Menggunakan TF-IDF Vectorizer untuk mengubah fitur teks (penulis, penerbit) menjadi vektor numerik dan menghitung cosine similarity antara buku-buku.

- **Solution Approach 2: Collaborative Filtering**  
  - **Deskripsi**:  
    Pendekatan ini merekomendasikan buku berdasarkan preferensi pengguna lain yang memiliki pola rating yang serupa. Model ini menggunakan embedding untuk merepresentasikan pengguna dan buku, kemudian memprediksi rating yang mungkin diberikan oleh pengguna terhadap buku yang belum mereka baca.  
  - **Keuntungan**:  
    Dapat memberikan rekomendasi yang personal dan akurat berdasarkan interaksi pengguna dengan buku.  
  - **Implementasi**:  
    Menggunakan model neural network dengan embedding layer untuk mempelajari representasi pengguna dan buku, serta memprediksi rating berdasarkan interaksi historis.

- **Solution Approach 3: Hybrid Approach**  
  - **Deskripsi**:  
    Menggabungkan keunggulan dari content-based filtering dan collaborative filtering untuk memberikan rekomendasi yang lebih komprehensif. Misalnya, menggunakan collaborative filtering untuk pengguna dengan data rating yang cukup dan content-based filtering untuk pengguna baru atau dengan sedikit data rating.  
  - **Keuntungan**:  
    Meningkatkan akurasi rekomendasi dan mengatasi masalah cold start serta ketidakmerataan data rating.  
  - **Implementasi**:  
    Menggabungkan hasil rekomendasi dari kedua pendekatan dan memberikan rekomendasi akhir berdasarkan skor gabungan atau prioritas tertentu.

---

## Data Understanding

Dataset yang digunakan dalam proyek ini terdiri dari tiga file utama: **Users.csv**, **Ratings.csv**, dan **Books.csv**. Dataset ini berisi informasi tentang pengguna, rating buku, dan detail buku. Dataset dapat diunduh melalui tautan berikut:  
[Book Recommendation Dataset (Kaggle)](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)
- [Users.csv](https://drive.google.com/uc?id=1Ppo-eHXxPf_SsmIar7lcxVFB7dT3Y3dC)  
- [Ratings.csv](https://drive.google.com/uc?id=1y7uCmxZpnITE701PJDTfOtz6ZXoJEgKi)  
- [Books.csv](https://drive.google.com/uc?id=1JC_aDsDWmFcDPLmEmCNgJ_tyYfg6xBA5)  

### Jumlah Data dan Kondisi Data
- **Users.csv**: Terdiri dari 278.853 baris dan 3 kolom (User-ID, Location, Age).  
- **Ratings.csv**: Terdiri dari 1.149.780 baris dan 3 kolom (User-ID, ISBN, Book-Rating).  
- **Books.csv**: Terdiri dari 2.193 baris dan 11 kolom (ISBN, Book-Title, Book-Author, Year-Of-Publication, Publisher, Image-URL-S, Image-URL-M, Image-URL-L).  

Dataset ini memiliki beberapa masalah seperti missing values, duplikasi data, dan outlier yang perlu ditangani sebelum digunakan untuk membangun model.

### Variabel atau Fitur pada Dataset
Berikut adalah variabel-variabel yang terdapat pada dataset:

#### Users.csv
- **User-ID**: ID unik yang mengidentifikasi setiap pengguna.  
- **Location**: Lokasi pengguna (berupa string yang menggambarkan kota, negara, dll.).  
- **Age**: Usia pengguna (dalam tahun).  

#### Ratings.csv
- **User-ID**: ID unik pengguna yang memberikan rating.  
- **ISBN**: ISBN buku yang diberi rating.  
- **Book-Rating**: Rating yang diberikan oleh pengguna (skala 0-10).  

#### Books.csv
- **ISBN**: Nomor ISBN buku.  
- **Book-Title**: Judul buku.  
- **Book-Author**: Penulis buku.  
- **Year-Of-Publication**: Tahun buku diterbitkan.  
- **Publisher**: Penerbit buku.  
- **Image-URL-S**: URL gambar sampul buku (ukuran kecil).  
- **Image-URL-M**: URL gambar sampul buku (ukuran sedang).  
- **Image-URL-L**: URL gambar sampul buku (ukuran besar).  

### Exploratory Data Analysis (EDA)
Beberapa tahapan EDA yang dilakukan untuk memahami data meliputi:

#### Visualisasi Distribusi Usia Pengguna
- **Insight**: Mayoritas pengguna berada pada rentang usia 20-50 tahun.  
- **Visualisasi**: Histogram distribusi usia pengguna.

![image](https://github.com/user-attachments/assets/848368a0-24b2-4181-82d3-3a3f669b60c0)

#### Visualisasi Distribusi Rating Buku
- **Insight**: Banyak buku memiliki rating 0, diikuti oleh rating 8 dan 10.  
- **Visualisasi**: Bar plot distribusi rating buku.  

![image](https://github.com/user-attachments/assets/d739952a-6367-4bb5-a465-ffdf975005dc)

#### Visualisasi Top 10 Lokasi Pengguna
- **Insight**: Mayoritas pengguna yang memberikan rating berasal dari daerah Eropa.  
- **Visualisasi**: Bar plot top 10 lokasi pengguna.  

![image](https://github.com/user-attachments/assets/0ce013fd-a42e-4ab0-91d6-9228e018b362)

#### Visualisasi Jumlah Banyak Rating Per user
- **Insight**: mayoritas user cuma menulis sekitar < 50 rating. kebanyakan user memberi rating minimal sekali saja.
- **Visualisasi**: Line Graph Banyak Rating Per User.
  
![image](https://github.com/user-attachments/assets/d4a25786-d269-42b5-b6f6-b53295475b7c)


#### Visualisasi Distribusi Tahun Penerbitan Buku
- **Insight**: Banyak buku dalam dataset diterbitkan sekitar tahun 2000.  
- **Visualisasi**: Histogram distribusi tahun penerbitan buku.  

![image](https://github.com/user-attachments/assets/0fbccf5d-690b-440c-8571-02fb1e401508)

#### Visualisasi Top 10 Penulis dan Penerbit
- **Insight**: Agatha Christie adalah penulis dengan buku terbanyak, dan Harlequin adalah penerbit dengan buku terbanyak.  
- **Visualisasi**: Bar plot top 10 penulis dan penerbit.

![image](https://github.com/user-attachments/assets/2955d8b6-3fd2-4f1c-b154-04c8269889e1)
![image](https://github.com/user-attachments/assets/8842fdb1-4984-4e5a-b8e2-751240fd7a36)


#### Visualisasi Top 20 Books with the Most Ratings
- **Insight**: Terdapat relasi antar ISBN dan rating.
- **Visualisasi**: Bar plot Top 20 Books with the Most Ratings.

![image](https://github.com/user-attachments/assets/bfb99baf-bb38-4d17-b3d7-7334c06db598)

---

## Data Preparation

Pada bagian ini, dilakukan beberapa tahapan data preparation untuk memastikan data siap digunakan dalam pembangunan model. Berikut adalah teknik dan proses yang dilakukan:

### 1. **Penggabungan Dataset**
   - **Proses**: Menggabungkan dataset **Users.csv**, **Ratings.csv**, dan **Books.csv** menjadi satu dataframe menggunakan kolom **User-ID** dan **ISBN** sebagai kunci penggabungan.  
   - **Alasan**: Penggabungan diperlukan untuk menghubungkan informasi pengguna, rating, dan buku dalam satu dataframe sehingga memudahkan analisis dan pemodelan.

### 2. **Penanganan Missing Values**
   - **Proses**:  
     - Mengecek jumlah missing values pada setiap kolom.  
     - Menghapus baris yang memiliki missing values pada kolom **Age** karena data usia penting untuk analisis demografi pengguna.  
     - Menghapus missing values pada kolom lain seperti **ISBN**, **Book-Title**, **Book-Author**, **Year-Of-Publication**, dan **Publisher** karena data ini diperlukan untuk membangun sistem rekomendasi.  
   - **Alasan**: Missing values dapat mengurangi kualitas data dan mempengaruhi akurasi model. Penanganan ini memastikan data yang digunakan bersih dan lengkap.

### 3. **Penanganan Duplikasi Data**
   - **Proses**:  
     - Mengecek jumlah data duplikat.  
     - Menghapus data duplikat jika ditemukan.  
   - **Alasan**: Data duplikat dapat menyebabkan bias dalam analisis dan pemodelan. Menghapus duplikat memastikan setiap entri data unik.

### 4. **Penanganan Outlier**
   - **Proses**:  
     - Mengecek outlier pada kolom **Age** dan **Year-Of-Publication** menggunakan boxplot.  
     - Menghapus outlier dengan metode IQR (Interquartile Range) untuk memastikan data berada dalam rentang yang wajar.  
   - **Alasan**: Outlier dapat mempengaruhi hasil analisis dan pemodelan. Menghapus outlier membantu meningkatkan kualitas data.

### 5. **Konversi Tipe Data**
   - **Proses**:  
     - Mengubah kolom **Year-Of-Publication** menjadi tipe data numerik (integer) untuk memudahkan analisis.  
     - Mengubah kolom **User-ID** dan **ISBN** menjadi tipe data kategori untuk mengoptimalkan penggunaan memori.  
   - **Alasan**: Konversi tipe data memastikan data sesuai dengan kebutuhan analisis dan pemodelan serta mengoptimalkan performa komputasi.

### 6. **Normalisasi Rating**
   - **Proses**:  
     - Melakukan normalisasi pada kolom **Book-Rating** ke skala 0-1 menggunakan min-max normalization.  
   - **Alasan**: Normalisasi membantu menyamakan skala data sehingga memudahkan proses pemodelan, terutama pada algoritma yang sensitif terhadap skala data.

### 7. **Pembuatan Matriks Interaksi Pengguna-Buku**
   - **Proses**:  
     - Membuat matriks interaksi pengguna-buku dalam bentuk sparse matrix menggunakan library **scipy.sparse**.  
   - **Alasan**: Matriks interaksi ini diperlukan untuk membangun model collaborative filtering, di mana matriks ini merepresentasikan hubungan antara pengguna dan buku berdasarkan rating.

### 8. **Filtering Data**
   - **Proses**:  
     - Memfilter pengguna dan buku yang memiliki jumlah rating kurang dari 5 untuk mengurangi noise dan meningkatkan kualitas data.  
   - **Alasan**: Data dengan terlalu sedikit rating dapat menyebabkan rekomendasi yang tidak akurat. Filtering ini memastikan hanya data yang relevan yang digunakan.

### 9. **Pembagian Data Training dan Testing**
   - **Proses**:  
     - Membagi data menjadi training set (80%) dan testing set (20%) menggunakan **train_test_split** dari library **sklearn**.  
   - **Alasan**: Pembagian data diperlukan untuk melatih model dan menguji performanya secara terpisah, sehingga dapat menghindari overfitting.

### 10. **Pembuatan Fitur Gabungan untuk Content-Based Filtering**
   - **Proses**:  
     - Menggabungkan kolom **Book-Author** dan **Publisher** menjadi satu kolom baru (**combined_features**) untuk digunakan dalam TF-IDF Vectorizer.  
   - **Alasan**: Fitur gabungan ini digunakan untuk menghitung kesamaan konten antar buku dalam pendekatan content-based filtering.

---

## Modeling

Pada tahapan ini, dua solusi sistem rekomendasi dibangun menggunakan pendekatan yang berbeda: **Content-Based Filtering** dan **Collaborative Filtering**. Kedua pendekatan ini digunakan untuk memberikan rekomendasi buku kepada pengguna berdasarkan data yang telah dipersiapkan sebelumnya.

### 1. **Content-Based Filtering**

#### Deskripsi Model
- **Pendekatan**: Menggunakan TF-IDF Vectorizer untuk mengubah fitur teks (seperti penulis dan penerbit) menjadi vektor numerik. Kemudian, menghitung cosine similarity antara buku-buku untuk menemukan buku yang mirip berdasarkan konten.
- **Output**: Rekomendasi top-N buku berdasarkan kesamaan konten dengan buku yang telah disukai oleh pengguna.

#### Implementasi
```python
def get_recommendations(title, cosine_sim=cosine_sim):
    idx = filtered_df[filtered_df['Book-Title'] == title].index[0]
    sim_scores = list(enumerate(cosine_sim[idx]))
    sim_scores = sorted(sim_scores, key=lambda x: x[1], reverse=True)
    sim_scores = sim_scores[1:11]  # Ambil 10 buku teratas
    book_indices = [i[0] for i in sim_scores]
    return filtered_df['Book-Title'].iloc[book_indices]

# Contoh penggunaan
top_n_recommendations_content = get_recommendations('Harry Potter and the Prisoner of Azkaban (Book 3)')
print(top_n_recommendations_content)
```

### 2. **Collaborative Filtering**

#### Deskripsi Model
- **Pendekatan**: Menggunakan model neural network yang memanfaatkan embedding untuk merepresentasikan pengguna dan buku. Model ini memprediksi rating yang mungkin diberikan oleh pengguna terhadap buku yang belum mereka baca.
- **Output**: Rekomendasi top-N buku berdasarkan prediksi rating untuk buku yang belum dinilai oleh pengguna.

#### Implementasi
```python
# Menggunakan model RecommenderNet yang telah didefinisikan sebelumnya
user_id_to_predict = 0  # ID pengguna yang ingin diprediksi
user_input = np.array([[user_id_to_predict]])
book_input = np.arange(len(book_ids))

predicted_ratings = model.predict({'user_input': np.repeat(user_input, len(book_ids), axis=0), 'book_input': book_input})

# Membuat DataFrame rekomendasi
recommendations = pd.DataFrame({'book_index': book_input, 'predicted_rating': predicted_ratings.flatten()})
top_n_recommendations_collaborative = recommendations.sort_values(by='predicted_rating', ascending=False).head(10)

# Mengambil ISBN dan judul buku
top_n_recommendations_collaborative['ISBN'] = top_n_recommendations_collaborative['book_index'].map(lambda x: merged_df['ISBN'].cat.categories[x])
top_n_recommendations_collaborative = top_n_recommendations_collaborative.merge(books_df, on='ISBN', how='inner')
print(top_n_recommendations_collaborative[['ISBN', 'Book-Title', 'predicted_rating']])
```

### Kelebihan dan Kekurangan

#### Content-Based Filtering
- **Kelebihan**:
  - Tidak memerlukan data rating dari pengguna lain, sehingga dapat memberikan rekomendasi yang relevan untuk pengguna baru (cold start problem).
  - Rekomendasi didasarkan pada fitur yang jelas dan dapat dipahami, seperti penulis dan penerbit.

- **Kekurangan**:
  - Rekomendasi cenderung terbatas pada buku-buku yang mirip dengan yang sudah dinilai, sehingga kurang beragam.
  - Memerlukan fitur yang baik dan representatif untuk menghasilkan rekomendasi yang akurat.

#### Collaborative Filtering
- **Kelebihan**:
  - Dapat memberikan rekomendasi yang lebih personal dan akurat berdasarkan pola rating pengguna lain.
  - Mampu menemukan hubungan yang tidak terlihat antara pengguna dan buku, sehingga dapat memberikan rekomendasi yang lebih beragam.

- **Kekurangan**:
  - Memerlukan data rating yang cukup untuk setiap pengguna dan buku, sehingga dapat mengalami masalah pada pengguna baru atau buku baru (cold start problem).
  - Rentan terhadap bias jika ada pengguna atau buku yang memiliki rating yang tidak merata.

### Kesimpulan
Kedua pendekatan memiliki kelebihan dan kekurangan masing-masing. Content-Based Filtering lebih baik untuk pengguna baru, sementara Collaborative Filtering dapat memberikan rekomendasi yang lebih kaya dan beragam jika data rating cukup. Menggabungkan kedua pendekatan dalam sistem rekomendasi hybrid dapat menjadi solusi yang efektif untuk mengatasi masalah yang ada.

---

## Evaluation

Pada bagian ini, kami akan membahas metrik evaluasi yang digunakan untuk menilai performa sistem rekomendasi yang dibangun, serta menjelaskan hasil proyek berdasarkan metrik tersebut.

### Metrik Evaluasi

1. **Mean Squared Error (MSE)**
   - **Deskripsi**: MSE mengukur rata-rata kesalahan kuadrat antara nilai yang diprediksi dan nilai aktual. Metrik ini memberikan gambaran seberapa jauh prediksi model dari nilai sebenarnya.
   - **Formula**: 
     \[
     \text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
     \]
     di mana:
     - \(y_i\) adalah nilai aktual (rating yang diberikan pengguna).
     - \(\hat{y}_i\) adalah nilai prediksi (rating yang diprediksi oleh model).
     - \(n\) adalah jumlah total prediksi.
   - **Cara Kerja**: MSE menghitung selisih kuadrat antara setiap prediksi dan nilai aktual, kemudian mengambil rata-ratanya. Nilai MSE yang lebih rendah menunjukkan model yang lebih baik.

2. **Root Mean Squared Error (RMSE)**
   - **Deskripsi**: RMSE mengukur akar kuadrat dari rata-rata kesalahan kuadrat antara nilai yang diprediksi dan nilai aktual. Metrik ini lebih sensitif terhadap outlier dibandingkan MSE.
   - **Formula**: 
     \[
     \text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
     \]
   - **Cara Kerja**: RMSE menghitung selisih kuadrat antara setiap prediksi dan nilai aktual, kemudian mengambil rata-ratanya dan menghitung akar kuadratnya. RMSE yang lebih rendah menunjukkan model yang lebih baik.

### Hasil Proyek Berdasarkan Metrik Evaluasi

Setelah menerapkan model dan melakukan evaluasi, berikut adalah hasil yang diperoleh:

- **Mean Squared Error (MSE)**: 
  - Hasil MSE yang diperoleh adalah 0.0282. Ini menunjukkan bahwa, secara rata-rata, prediksi rating model menyimpang sekitar 0.0282 dari rating aktual. Nilai ini menunjukkan performa yang cukup baik, tetapi masih ada ruang untuk perbaikan.

- **Root Mean Squared Error (RMSE)**: 
  - Hasil RMSE yang diperoleh adalah **0.168**. RMSE yang diperoleh menunjukkan bahwa model telah menghasilkan prediksi yang cukup akurat secara keseluruhan. Meskipun ada beberapa variasi pada prediksi tertentu, nilai RMSE yang relatif rendah ini menunjukkan performa model yang baik. Namun, masih ada peluang untuk lebih menyempurnakan model guna mencapai akurasi yang lebih tinggi.

### Kesimpulan
Metrik evaluasi yang digunakan memberikan gambaran yang jelas tentang performa sistem rekomendasi. Meskipun hasil menunjukkan bahwa model sudah cukup baik, ada ruang untuk perbaikan, terutama dalam mengurangi kesalahan prediksi dan meningkatkan relevansi rekomendasi. Dengan melakukan tuning model dan eksplorasi lebih lanjut terhadap data, diharapkan performa sistem rekomendasi dapat ditingkatkan.

---

**---Ini adalah bagian akhir laporan---**
