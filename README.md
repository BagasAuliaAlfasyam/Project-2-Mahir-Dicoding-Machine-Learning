# Laporan Proyek Machine Learning - Bagas Aulia Alfasyam

## Project Overview

<!-- markdownlint-disable MD033 -->
<div style="text-align: justify;">
<!-- markdownlint-enable MD033 -->

![Steam](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/download.jpeg)

Steam, yang merupakan platform distribusi game yang dikembangkan oleh Valve Corporation, telah menjadi tempat utama untuk jual-beli permainan video game di seluruh dunia. Hingga tahun 2022, lebih dari 10.000 permainan telah diterbitkan di platform Steam (Mulachela, Rizki, & Wahyuddin, 2020). Perkembangan teknologi di awal 90-an melemahkan monopoli Jepang atas industri game. Banyak perusahaan multinasional (MNC) dari negara lain turut berkontribusi dalam melemahkan dominasi Jepang di pasar industri game. Misalnya, di Amerika Serikat, meskipun negara ini tidak memimpin di industri konsol game, pengembang dan penerbit lokal mereka sangat berpengaruh di sektor industri game komputer. Pengembang dan MNC asal Amerika Serikat telah menerbitkan game-game komputer yang sukses hingga saat ini. Salah satu game tersebut mencapai kesuksesan di Korea Selatan, yang kemudian berkontribusi dalam penciptaan kompetisi game (e-sports) di negara tersebut [(Mulachela, Rizki, & Wahyuddin, 2020)](https://jtiik.ub.ac.id/index.php/jtiik/article/view/8503).

Seiring dengan perkembangan industri game, kebutuhan akan sistem rekomendasi game yang efektif menjadi semakin penting. Sistem rekomendasi game dapat membantu pemain menemukan game baru yang sesuai dengan preferensi mereka. Tiga pendekatan utama dalam sistem rekomendasi adalah content-based filtering, collaborative filtering, dan hybrid recommendation system [(Syamkalla, Khomsah, & Nur, 2024)](https://jtiik.ub.ac.id/index.php/jtiik/article/view/8503).

Content-based filtering bekerja dengan menganalisis berbagai fitur dari game yang disukai oleh pengguna dan merekomendasikan game lain yang memiliki fitur serupa. Metode ini mengandalkan data deskriptif seperti genre, tema, dan mekanika permainan [(Ricci, Rokach, & Shapira, 2011)](https://link.springer.com/chapter/10.1007/978-0-387-85820-3_1).

Di sisi lain, collaborative filtering bekerja berdasarkan kemiripan preferensi di antara pengguna. Metode ini menemukan pola dari perilaku pengguna sebelumnya untuk memberikan rekomendasi yang relevan. Sistem ini sering digunakan dalam platform besar seperti Steam untuk menyediakan rekomendasi game yang personal [(Resnick et al., 1994)](https://dl.acm.org/doi/10.1145/192844.192905).

Hybrid recommendation system menggabungkan pendekatan content-based filtering dan collaborative filtering untuk memberikan rekomendasi yang lebih akurat dan personal. Sistem ini memanfaatkan keunggulan dari kedua metode untuk mengatasi keterbatasan masing-masing [(Burke, 2002)](https://link.springer.com/article/10.1023/A:1021240730564).

Dengan adanya berbagai pendekatan ini, sistem rekomendasi game dapat memberikan pengalaman yang lebih baik bagi pengguna dengan menyarankan game yang lebih relevan dan menarik sesuai dengan preferensi individu.

## Business Understanding

Pengembangan sistem rekomendasi games memiliki potensi besar untuk memberikan berbagai keuntungan bagi pengguna dan platform distribusi game. Dengan mengimplementasikan tiga pendekatan berbeda - Content-based Filtering, Collaborative Filtering, dan Hybrid Recommendation System - project ini bertujuan untuk memberikan rekomendasi game yang lebih akurat dan personal.

### Problem Statements

1. Bagaimana menerapkan Exploratory Data Analysis (EDA) pada dataset yang berhubungan dengan sistem rekomendasi?
2. Bagaimana cara mengembangkan sistem rekomendasi game yang dapat merekomendasikan game berdasarkan konten dan preferensi pengguna?
3. Bagaimana metode Content-based, Collaborative, dan Hybrid Filtering dapat diintegrasikan untuk menghasilkan rekomendasi yang lebih komprehensif?
4. Bagaimana cara mengukur efektivitas dan akurasi dari masing-masing metode rekomendasi?
5. Bagaimana sistem rekomendasi dapat mempertimbangkan berbagai fitur seperti tags, deskripsi, platform, dan rating pengguna?

### Goals

1. Melakukan Exploratory Data Analysis (EDA) mendalam pada dataset game untuk mengidentifikasi pola, distribusi, dan karakteristik data.
2. Mengembangkan sistem rekomendasi berbasis konten menggunakan Cosine Similarity.
3. Membangun sistem rekomendasi kolaboratif berbasis similarity pengguna dan game.
4. Merancang Hybrid Recommendation System menggunakan Deep Learning.
5. Mengukur performa sistem rekomendasi menggunakan metrik Mean Absolute Error (MAE).
6. Menghasilkan rekomendasi game yang personal dan akurat.

### Solution Statements

1. **Exploratory Data Analysis (EDA) pada Dataset Sistem Rekomendasi**

   Proses EDA akan dilakukan secara komprehensif untuk memahami karakteristik dataset game. Analisis akan mencakup statistik deskriptif yang mendalam, mengidentifikasi pola dan korelasi unik dalam dataset. Melalui teknik visualisasi seperti histogram, boxplot, dan scatter plot, akan diungkap distribusi berbagai fitur game. Tahapan ini juga akan fokus pada deteksi dan penanganan missing values, serta analisis mendalam tentang frekuensi tags, genre, dan platform game untuk memberikan wawasan fundamental sebelum membangun sistem rekomendasi.

2. **Pengembangan Sistem Rekomendasi Berbasis Konten menggunakan Cosine Similarity**

   Sistem rekomendasi berbasis konten akan dikembangkan melalui serangkaian tahap preprocessing yang cermat. Dimulai dengan pembersihan teks, tokenisasi, dan stemming, proses akan berlanjut dengan ekstraksi fitur menggunakan TF-IDF vectorization. Cosine Similarity akan menjadi metode utama dalam menghitung kesamaan antar game, mempertimbangkan berbagai aspek seperti judul, deskripsi, dan tags. Algoritma akan dirancang untuk menghasilkan sepuluh rekomendasi teratas yang paling mirip secara konten, memberikan pengalaman rekomendasi yang personal dan akurat.

3. **Collaborative Filtering dengan Pendekatan User dan Item Similarity**

   Pendekatan collaborative filtering akan diimplementasikan melalui dua metode utama: user-based dan item-based. Pada pendekatan user-based, sistem akan membangun matriks preferensi pengguna dan menghitung Cosine Similarity antar profil pengguna untuk menemukan pola rating yang serupa. Sementara itu, metode item-based akan fokus pada konstruksi matriks similarity antar game, mengidentifikasi game serupa berdasarkan pola rating yang ada. Kedua pendekatan ini akan saling melengkapi untuk menghasilkan rekomendasi yang komprehensif.

4. **Hybrid Recommendation System menggunakan Deep Learning**

   Sistem rekomendasi hibrid akan dibangun menggunakan arsitektur neural network yang canggih. Model akan memanfaatkan embedding layer untuk mengolah fitur teks, menerapkan multi-label encoding untuk tags game, dan mengintegrasikan fitur platform serta deskriptif. Struktur jaringan akan mencakup layer dense untuk agregasi fitur kompleks, dengan fungsi aktivasi sigmoid yang memungkinkan prediksi rekomendasi yang presisi. Pendekatan ini bertujuan menggabungkan kekuatan pemrosesan berbagai sumber informasi dalam satu model terintegrasi.

5. **Analisis Multi-Fitur untuk Sistem Rekomendasi**

   Strategi analisis multi-fitur akan mengembangkan pendekatan pembobotan dinamis yang kompleks. Sistem akan melakukan normalisasi dan integrasi fitur dari berbagai sumber, mempertimbangkan secara komprehensif aspek seperti tags game, deskripsi, platform, rating pengguna, genre, dan tingkat popularitas. Implementasi adaptive feature weighting akan memungkinkan model untuk secara cerdas menyesuaikan bobot setiap fitur berdasarkan relevansinya, dengan analisis mendalam terhadap korelasi antar fitur untuk mengoptimalkan akurasi rekomendasi.

6. **Evaluasi Performa Sistem Rekomendasi**

   Tahap evaluasi akan dilakukan secara menyeluruh dengan fokus utama pada perhitungan Mean Absolute Error (MAE) untuk mengukur akurasi model. Proses cross-validation akan digunakan untuk memvalidasi konsistensi performa, sementara analisis komparatif akan membandingkan metode rekomendasi berbasis konten, kolaboratif, dan hibrid. Pengujian akan mencakup kemampuan model dalam menghasilkan rekomendasi personal serta menguji robustness terhadap berbagai variasi dataset, memberikan gambaran komprehensif tentang efektivitas sistem rekomendasi yang dikembangkan.

## Data Understanding

Pada project yg dibuat ini dataset diambil dari situs repository terbuka kaggle [Tautan](https://www.kaggle.com/api/v1/datasets/download/antonkozyriev/game-recommendations-on-steam) dengan keterangan seperti table di bawah ini.

### **Informasi Dataset**

| Jenis          | Keterangan                                                                                                                   |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Title          | [Game Recommendations on Steam](https://www.kaggle.com/api/v1/datasets/download/antonkozyriev/game-recommendations-on-steam) |
| Source         | [Kaggle](https://www.kaggle.com/datasets/antonkozyriev/game-recommendations-on-steam)                                        |
| Maintainer     | [Anton Kozyriev](https://www.kaggle.com/antonkozyriev)                                                                       |
| License        | Database: Open Database, Contents: Database Contents                                                                         |
|                | Publik                                                                                                                       |
| Tags           | Tabular, Games, Video Games, Exploratory Data Analysis, Recommender Systems                                                  |
| File Available | `games.csv`, `users.csv`, `recommendations.csv`, `games_metadata.json`                                                       |
| Usability      | 10.00                                                                                                                        |

### Variabel-variabel dataset adalah sebagai berikut

#### Dataset Games `games.csv`

| Kolom          | Deskripsi                                                                  |
| -------------- | -------------------------------------------------------------------------- |
| app_id         | Identifikasi unik untuk setiap game di Steam                               |
| title          | Judul resmi game                                                           |
| date_release   | Tanggal rilis game                                                         |
| win            | Menunjukkan apakah game tersedia untuk sistem operasi Windows (true/false) |
| mac            | Menunjukkan apakah game tersedia untuk sistem operasi Mac (true/false)     |
| linux          | Menunjukkan apakah game tersedia untuk sistem operasi Linux (true/false)   |
| rating         | Peringkat umum game berdasarkan ulasan pengguna                            |
| positive_ratio | Persentase ulasan positif dari total ulasan                                |
| user_reviews   | Jumlah total ulasan pengguna                                               |
| price_final    | Harga akhir game                                                           |
| price_original | Harga asli game sebelum diskon                                             |
| discount       | Persentase diskon yang diterapkan                                          |
| steam_deck     | Menunjukkan apakah game kompatibel dengan Steam Deck (true/false)          |

**Jumlah Baris dan Kolom** : **50872 x 13**

Dataset game ini menyediakan informasi komprehensif tentang berbagai game di platform Steam, mencakup aspek teknis, komersial, dan penerimaan pengguna. Setiap kolom memberikan dimensi unik yang dapat dimanfaatkan untuk analisis mendalam dan pengembangan sistem rekomendasi. Informasi platform (Windows, Mac, Linux, Steam Deck) memungkinkan pemahaman tentang aksesibilitas game, sementara metrik seperti rating, rasio ulasan positif, dan jumlah ulasan pengguna memberikan wawasan tentang kualitas dan popularitas game. Data harga dan diskon menambahkan lapisan analisis komersial, memungkinkan eksplorasi strategi pricing dan daya tarik game dari perspektif ekonomi. Dengan demikian, dataset ini tidak hanya sebagai sumber informasi, tetapi juga sebagai fondasi untuk mengembangkan sistem rekomendasi cerdas yang mempertimbangkan berbagai faktor yang memengaruhi preferensi pengguna game.

#### Dataset Users `users.csv`

| Kolom    | Deskripsi                                 |
| -------- | ----------------------------------------- |
| user_id  | Identifikasi unik untuk setiap pengguna   |
| products | Jumlah produk/game yang dimiliki pengguna |
| reviews  | Jumlah ulasan yang dibuat pengguna        |

**Jumlah Baris dan Kolom :** **14306064 x 3**

Dataset Users ini memberikan informasi kritis untuk memahami karakteristik dan perilaku pengguna dalam konteks platform game. Setiap kolom menyediakan perspektif unik tentang interaksi pengguna dengan game. Jumlah produk atau game yang dimiliki seorang pengguna mengindikasikan tingkat keterlibatan dan minat mereka dalam platform, sementara jumlah ulasan yang dibuat menunjukkan seberapa aktif mereka berpartisipasi dalam komunitas game. Dengan menganalisis dataset ini, sistem rekomendasi dapat dikembangkan untuk mengidentifikasi pola preferensi pengguna, mengelompokkan pengguna berdasarkan perilaku gaming mereka, dan menciptakan pengalaman rekomendasi yang sangat personal. Analisis mendalam dapat mengungkap tren seperti hubungan antara jumlah game yang dimiliki dengan frekuensi ulasan, preferensi genre, dan intensitas keterlibatan pengguna dalam ekosistem game.

#### Dataset Recommendations `recommendations.csv`

| Kolom          | Deskripsi                                                   |
| -------------- | ----------------------------------------------------------- |
| app_id         | Identifikasi game yang direview                             |
| helpful        | Jumlah pengguna yang menganggap review ini membantu         |
| funny          | Jumlah pengguna yang menganggap review ini lucu             |
| date           | Tanggal review dibuat                                       |
| is_recommended | Apakah pengguna merekomendasikan game tersebut (True/False) |
| hours          | Jumlah jam bermain game                                     |
| user_id        | Identifikasi pengguna yang membuat review                   |
| review_id      | Identifikasi unik untuk setiap review                       |

**Jumlah Baris dan Kolom :** **41154794 x 8**

Dataset Recommendations ini merupakan sumber informasi kritis untuk memahami dinamika interaksi pengguna dengan game di platform. Setiap kolom memberikan dimensi unik tentang pengalaman pengguna, mulai dari jumlah jam bermain hingga persepsi mereka tentang game. Metrik seperti helpful dan funny menggambarkan aspek sosial dan interaktif dari komunitas game, sementara is_recommended memberikan indikasi langsung tentang kualitas dan kepuasan pengguna terhadap game tertentu. Jumlah jam bermain menjadi parameter penting untuk mengukur keterlibatan dan minat pengguna. Dengan menganalisis dataset ini, peneliti dan pengembang dapat membangun sistem rekomendasi yang canggih, mengidentifikasi pola preferensi game, dan menciptakan pengalaman yang sangat personal bagi setiap pengguna.

#### Dataset `games_metadata.json`

| Kolom       | Deskripsi                                                 |
| ----------- | --------------------------------------------------------- |
| app_id      | Identifikasi unik untuk setiap game                       |
| description | Deskripsi singkat tentang game                            |
| tags        | Kategori atau label yang menggambarkan karakteristik game |

**Jumlah Baris dan Kolom :** **50872 x 3**

Dataset Games Metadata menyediakan informasi esensial yang memperkaya pemahaman tentang karakteristik game secara mendalam. Deskripsi singkat memberikan gambaran konseptual tentang game, memungkinkan analisis semantik dan ekstraksi fitur yang kompleks. Tags berperan krusial dalam mengkategorikan game, memberikan dimensi tambahan untuk klasifikasi dan rekomendasi. Setiap tag dapat menangkap aspek unik seperti genre, gaya gameplay, tema, atau mekanika permainan, yang memungkinkan sistem rekomendasi untuk memahami nuansa dan keunikan setiap game. Kombinasi antara app_id, description, dan tags menciptakan fondasi yang kuat untuk pengembangan sistem rekomendasi berbasis konten yang canggih, memungkinkan analisis mendalam tentang kesamaan game, preferensi pengguna, dan pola konsumsi game yang kompleks.

### Data Cleaning Process

#### Pengecekan Missing Values

```python
# Pengecekan Missing Values
games.isnull().sum()
users.isnull().sum()
recommendations.isnull().sum()
games_metadata.isnull().sum()
```

Tujuan utama dari tahap ini adalah memastikan kualitas data dengan mendeteksi dan mengevaluasi keberadaan nilai-nilai yang hilang (missing values) di setiap dataset. Dengan menggunakan fungsi `isnull().sum()`, kita dapat mengidentifikasi apakah terdapat kolom-kolom yang memiliki data tidak lengkap, yang dapat mempengaruhi akurasi dan reliabilitas analisis selanjutnya. Pemeriksaan menyeluruh ini membantu tim dalam membuat keputusan tentang strategi penanganan data yang tidak lengkap, baik melalui imputasi, penghapusan, atau metode lainnya.

#### Konversi List ke Tuple

```python
# Konversi list ke tuple di games_metadata
for col in games_metadata.columns:
    if games_metadata[col].apply(type).eq(list).any():
        games_metadata[col] = games_metadata[col].apply(tuple)
```

Tujuan transformasi ini adalah menstandarkan tipe data dalam dataset games_metadata. Dengan mengonversi kolom-kolom yang berisi tipe data list menjadi tuple, kita mencapai beberapa manfaat penting: (1) meningkatkan konsistensi tipe data, (2) memudahkan proses manipulasi dan analisis data, serta (3) mengoptimalkan penggunaan memori. Tuple lebih efisien dibandingkan list dalam hal kinerja dan immutability, yang sangat berguna dalam proses pengolahan data yang kompleks.

#### Pengecekan Duplikasi Data

```python
# Pengecekan Duplikasi Data
games_metadata.duplicated().sum()
games.duplicated().sum()
users.duplicated().sum()
recommendations.duplicated().sum()
```

Tujuan utama dari tahap ini adalah mengidentifikasi dan berpotensi menghapus data duplikat yang dapat menghasilkan bias dalam analisis. Duplikasi data dapat memengaruhi akurasi model, statistik, dan hasil analisis. Dengan menghitung jumlah baris duplikat di setiap dataset, kita dapat membuat keputusan tentang apakah perlu melakukan pembersihan dengan menghapus entri yang sama, yang pada gilirannya akan meningkatkan kualitas dan representativitas data.

#### Fungsi Pengurangan Memori

```python
# Fungsi Pengurangan Memori
def reduce_memory(data):
    for col in data.columns:
        if data[col].dtype == 'float64':
            data[col] = data[col].astype('float32')
        elif data[col].dtype == 'int64':
            data[col] = data[col].astype('int32')
    return data

# Implementasi Pengurangan Memori
data_game = reduce_memory(games)
data_users = reduce_memory(users)
data_recommendations = reduce_memory(recommendations)
data_games_metadata = reduce_memory(games_metadata)
```

Tujuan dari fungsi `reduce_memory()` adalah mengoptimalasi penggunaan sumber daya komputasi dengan mengurangi konsumsi memori. Dengan mengonversi tipe data numerik dari 64-bit ke 32-bit, kita mencapai beberapa keuntungan: (1) menurunkan kebutuhan memori, (2) meningkatkan kecepatan pemrosesan data, dan (3) memungkinkan pengolahan dataset yang lebih besar tanpa membebani sistem. Ini sangat penting dalam analisis big data atau pada sistem dengan keterbatasan sumber daya.

#### Sampling Recommendations

```python
# Sampling Recommendations
sample_recommendations = data_recommendations.sample(frac=0.001, random_state=42)

# Filter Users berdasarkan Recommendations
user_ids_in_recommendations = sample_recommendations['user_id'].unique()
filtered_data_users = data_users[data_users['user_id'].isin(user_ids_in_recommendations)]

print(f"Jumlah users yang dipertahankan: {filtered_data_users.shape[0]}")
```

Tujuan dari tahap sampling ini adalah mengurangi ukuran dataset sambil mempertahankan karakteristik statistik yang representatif. Dengan mengambil 0.1% dari total data secara acak, kita dapat: (1) mengurangi beban komputasi, (2) mempercepat proses analisis, dan (3) tetap menjaga integritas dan pola distribusi data asli. Sampling memungkinkan eksperimen dan analisis pada subset data yang dapat dikelola dengan tetap menjaga validitas hasil.

#### Konsistensi Recommendations dan Users

```python
# Filter User ID dan App ID
sample_data_users = data_users[data_users['user_id'].isin(sample_recommendations['user_id'])]
sample_recommendations = sample_recommendations[sample_recommendations['app_id'].isin(games['app_id'])]

# Pastikan Konsistensi Recommendations
consistent_recommendations = sample_recommendations[
    sample_recommendations['user_id'].isin(sample_data_users['user_id'])
]

print(f"Final jumlah rekomendasi: {consistent_recommendations.shape[0]}")
print(f"Final jumlah users: {sample_data_users.shape[0]}")
```

Tujuan dari tahap ini adalah memastikan konsistensi dan integritas referensial antara dataset recommendations, users, dan games. Dengan melakukan filtering dan validasi, kita dapat: (1) menghilangkan entri yang tidak valid, (2) memastikan setiap rekomendasi terkait dengan user dan game yang aktual, dan (3) mencegah potensi kesalahan dalam analisis atau pemodelan yang disebabkan oleh data yang tidak konsisten.

#### Cek Konsistensi User ID dan App ID

```python
# Cek Konsistensi User ID dan App ID
missing_users = set(consistent_recommendations['user_id']) - set(sample_data_users['user_id'])
print(f"User ID yang ada di consistent_recommendations tapi tidak ada di users: {len(missing_users)}")

missing_games = set(consistent_recommendations['app_id']) - set(games['app_id'])
print(f"Game ID yang ada di recommendations tapi tidak ada di games: {len(missing_games)}")
```

Tujuan dari pemeriksaan konsistensi ini adalah melakukan validasi akhir terhadap integritas data. Dengan memeriksa apakah terdapat user ID atau game ID yang tidak valid dalam dataset recommendations, kita dapat: (1) mengidentifikasi potensi anomali data, (2) memastikan kualitas dataset sebelum analisis, dan (3) mencegah kesalahan yang mungkin timbul dari data yang tidak lengkap atau tidak konsisten.

#### Menggabungkan Games dan Metadata Games

```python
# Menggabungkan Games dan Metadata Games
final_games = pd.merge(games, games_metadata, on='app_id', how='inner')
```

Tujuan akhir dari proses ini adalah membuat dataset komprehensif yang menggabungkan informasi dari games dan games_metadata. Dengan menggunakan inner join berdasarkan 'app_id', kita: (1) memastikan hanya game dengan informasi lengkap yang dipertahankan, (2) menciptakan dataset yang kaya akan detail, dan (3) menyiapkan data untuk analisis mendalam, pemodelan rekomendasi, atau eksplorasi game yang lebih lanjut.

### Finalisasi Cleaning Data

```python
final_games.isnull().sum()
sample_data_users.isnull().sum()
sample_recommendations.isnull().sum()

final_games.isna().sum()
sample_data_users.isna().sum()
sample_recommendations.isna().sum()
final_games.isna().sum()
```

Tahap finalisasi cleaning data bertujuan untuk melakukan pemeriksaan terakhir terhadap nilai-nilai yang hilang (null atau NA) di seluruh dataset. Menggunakan metode `isnull()` dan `isna()`, kita memverifikasi apakah proses pembersihan data sebelumnya telah berhasil menghilangkan semua nilai yang tidak lengkap.

Tujuan utamanya adalah:

- Memastikan konsistensi dataset
- Validasi akhir proses pembersihan data
- Persiapan dataset untuk analisis lanjutan

Jika pemeriksaan menunjukkan nol nilai hilang, dataset dianggap siap untuk tahap selanjutnya. Sebaliknya, jika ditemukan nilai hilang, mungkin diperlukan strategi tambahan seperti imputasi atau penghapusan baris.

## Exploratory Data Analysis (EDA)

### Exploratory Data Analysis - Deskripsi Variable

#### `final_games` info

| No  | Column         | Non-Null Count | Dtype   |
| --- | -------------- | -------------- | ------- |
|  0  | app_id         | 50872 non-null | int32   |
|  1  | title          | 50872 non-null | object  |
|  2  | date_release   | 50872 non-null | object  |
|  3  | win            | 50872 non-null | bool    |
|  4  | mac            | 50872 non-null | bool    |
|  5  | linux          | 50872 non-null | bool    |
|  6  | rating         | 50872 non-null | object  |
|  7  | positive_ratio | 50872 non-null | int32   |
|  8  | user_reviews   | 50872 non-null | int32   |
|  9  | price_final    | 50872 non-null | float32 |
|  10 | price_original | 50872 non-null | float32 |
|  11 | discount       | 50872 non-null | float32 |
|  12 | steam_deck     | 50872 non-null | bool    |
|  13 | description    | 50872 non-null | object  |
|  14 | tags           | 50872 non-null | object  |

Dataset `final_games` dan `games_metadata` yang sudah di gabungkan terdiri dari 14 fitur dengan struktur kompleks yang mencakup 4 fitur categorical (title, date_release, rating, description, tags), 6 fitur numerical (app_id, positive_ratio, user_reviews, price_final, price_original, discount), dan 4 fitur boolean untuk platform game (win, mac, linux, steam_deck). Com total 50.872 entri yang memiliki kelengkapan data 100% tanpa missing values, dataset ini menyediakan informasi komprehensif tentang game, termasuk metadata, ulasan pengguna, informasi harga, dan ketersediaan platform, yang memungkinkan analisis mendalam tentang karakteristik dan performa game.

#### `sample_data_users` Info

| No  | Column           | Non-Null Count  | Dtype   |
| --- | ---------------- | --------------- | ------- |
|  0  | user_id          |  40771 non-null | int32   |
|  1  | products         |  40771 non-null | int32   |
|  2  | reviews          |  40771 non-null | int32   |

Dataset `users` terdiri dari 3 fitur dengan struktur sederhana, mencakup 1 fitur integer (user_id, products, reviews) dengan total 40.771 entri. Total kelengkapan data 100% tanpa missing values, dataset ini memberikan informasi dasar tentang pengguna, fokus pada identifikasi pengguna, jumlah produk, dan jumlah review yang mereka lakukan, yang memungkinkan analisis awal tentang aktivitas dan interaksi pengguna dalam konteks game.

#### `sample_recommendations` Info

| No  | Column          | Non-Null Count  | Dtype  |
| --- | --------------- | --------------- | -----  |
|  0  |  app_id         | 41155 non-null  | int32  |
|  1  |  helpful        | 41155 non-null  | int32  |
|  2  |  funny          | 41155 non-null  | int32  |
|  3  |  date           | 41155 non-null  | object |
|  4  |  is_recommended | 41155 non-null  | bool   |
|  5  |  hours          | 41155 non-null  | float32|
|  6  |  user_id        | 41155 non-null  | int32  |
|  7  |  review_id      | 41155 non-null  | int32  |

Dataset `sample_recommendations` terdiri dari 8 fitur dengan struktura beragam, mencakup 5 fitur integer (app_id, helpful, funny, user_id, review_id), 1 fitur float (hours), 1 fitur object (date), dan 1 fitur boolean (is_recommended) dengan total 41.155 entri. Dataset memiliki kelengkapan data 100% tanpa missing values, memberikan informasi detail tentang rekomendasi game, termasuk aspek interaksi pengguna seperti jumlah review yang dianggap membantu, review lucu, status rekomendasi, dan durasi bermain game.

### Statistik Deskripttif

| Statistic     | app_id         | positive_ratio | user_reviews     | price_final | price_original | discount |
|---------------|----------------|----------------|------------------|-------------|----------------|----------|
| count         | 50,872         | 50,872         | 50,872           | 50,872      | 50,872         | 50,872   |
| mean          | 1,055,224      | 77.05          | 1,824.43         | 8.62        | 8.73           | 5.59     |
| std           | 610,324.9      | 18.25          | 40,073.52        | 11.51       | 11.51          | 18.61    |
| min           | 10             | 0.00           | 10               | 0.00        | 0.00           | 0.00     |
| 25%           | 528,737.5      | 67.00          | 19               | 0.99        | 0.99           | 0.00     |
| 50%           | 986,085        | 81.00          | 49               | 4.99        | 4.99           | 0.00     |
| 75%           | 1,524,895      | 91.00          | 206              | 10.99       | 11.99          | 0.00     |
| max           | 2,599,300      | 100.00         | 7,494,460        | 299.99      | 299.99         | 90.00    |

Dataset Games d; menunjukkan variasi signifikan dalam berbagai metrik. app_id memiliki rentang yang luas dari 10 hingga 2,599,300, dengan rata-rata 1,055,224. positive_ratio menunjukkan rata-rata ulasan positif sekitar 77%, dengan standar deviasi 18.25%. Variabel harga (price_final dan price_original) memiliki rata-rata sekitar $8.62, namun dengan rentang yang lebar dari $0 hingga $299.99, menandakan diversitas pricing game.

| Statistic     | user_id         | products       | reviews         |
|---------------|-----------------|----------------|-----------------|
| count         | 40,771          | 40,771         | 40,771          |
| mean          | 7,456,114       | 274.09         | 20.40           |
| std           | 4,014,007       | 626.77         | 83.88           |
| min           | 519             | 0.00           | 1.00            |
| 25%           | 4,277,404       | 50.00          | 2.00            |
| 50%           | 7,546,667       | 119.00         | 5.00            |
| 75%           | 10,979,680      | 272.00         | 15.00           |
| max           | 14,304,900      | 17,475.00      | 6,045.00        |

Dataset Users menggambarkan karakteristik pengguna dengan user_id tersebar dari 519 hingga 14,304,900. Rata-rata jumlah produk per pengguna adalah 274, dengan variasi besar (std 626.77). Jumlah review per pengguna relatif rendah, dengan rata-rata 20.40 review dan median hanya 5 review.

| Statistic     | app_id          | helpful        | funny          | hours          | user_id         | review_id      |
|---------------|-----------------|----------------|-----------------|----------------|-----------------|----------------|
| count         | 41,155          | 41,155         | 41,155          | 41,155         | 41,155          | 41,155         |
| mean          | 605,829.6       | 3.13           | 1.25            | 99.32          | 7,462,344       | 20,649,160     |
| std           | 474,459.4       | 31.30          | 26.72           | 174.06         | 4,013,506       | 11,887,220     |
| min           | 10              | 0.00           | 0.00            | 0.00           | 519             | 1,294          |
| 25%           | 254,700         | 0.00           | 0.00            | 7.60           | 4,290,241       | 10,291,900     |
| 50%           | 438,100         | 0.00           | 0.00            | 27.00          | 7,551,315       | 20,716,230     |
| 75%           | 945,360         | 0.00           | 0.00            | 97.20          | 10,994,280      | 30,840,180     |
| max           | 2,209,610       | 2,483.00       | 2,535.00        | 999.80         | 14,304,900      | 41,154,280     |

3 Table diatas memberikan informasi statistik pada masing-masing kolom di 3 dataset, antara lain:

- Count adalah jumlah sampel pada data.
- Mean adalah nilai rata-rata.
- Std adalah standar deviasi.
- Min yaitu nilai minimum setiap kolom.
- 25% adalah kuartil pertama. Kuartil adalah nilai yang menandai batas interval - dalam empat bagian sebaran yang sama.
- 50% adalah kuartil kedua, atau biasa juga disebut median (nilai tengah).
- 75% adalah kuartil ketiga.
- Max adalah nilai maksimum.

### Exploratory Data Analysis - Univariate Analysis

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-5.png?raw=true)

Pada visualisasi Type Anime di atas dapat disimpulkan bahwa Type Anime TV menduduki jumlah paling tinggi disusul Movie dan OVA dan paling lalu ada Type anime UNKNOWN dengan jumlah paling sedikit.

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-7.png?raw=true)

Pada Visualisasi Sudios Anime di atas didapati bahwa Top 5 distribusi Studio Anime terbanyak sebesar 42.3% Tidak diketahui (UNKNOWN) lalu 3,3% untuk Studio Toei Animation, 2.1% Studio Sunrise, 1.5% Studio J.C.Staff, 1.3% Shanghai Animation Film Studio dan 49.4% untuk studio lainnya.

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-8.png?raw=true)

Hasil visualisasi di atas dapat disimpulkan untuk top 10 anime teratas berdasarkan jumlah membernya mulai dari shingeki no kyojin hingga hunter x hunter.

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-9.png?raw=true)

Hasil visualisasi di atas di dapati untuk top 10 anime teratas berdasarkan skor paling tinggi jika diambil 10 teratas berdasarkan score maka hasilnya berbeda dengan 10 anime teratas berdasarkan jumlah membernya.

### Exploratory Data Analysis - Multivariate Analysis

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-10.png?raw=true)

Dari visualisasi di atas didapati nilai korelasi negatif sebesar -0.36 menunjukkan adanya **hubungan negatif sedang** antara jumlah Members dan Popularity. Ini berarti bahwa anime dengan jumlah Members yang lebih tinggi cenderung memiliki nilai Popularity yang lebih rendah.

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-11.png?raw=true)

Pada visualisasi di atas didapati nilai korelasi negatif -0.19 ini menunjukkan **hubungan yang lemah** antara jumlah Favorites dan Popularity. Korelasi negatif berarti bahwa ketika jumlah Favorites meningkat, nilai Popularity (peringkat) cenderung menurun.

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-12.png?raw=true)

Pada visualisasi di atas didapati nilai korelasi 0.773 menunjukkan adanya hubungan positif yang kuat antara jumlah Favorites dan Members. Ini berarti bahwa anime dengan jumlah Members yang tinggi cenderung juga memiliki jumlah Favorites yang tinggi.

## Data Preparation

Teknik Data preparation yang dilakukan terdiri dari:

- Data Preprocessing
- TF-IDF Vectorizer Data Anime
- Encoding Data User Rating
- Train-test-split Data User Rating

### Data Preprocessing

sebelumnya kita memiliki 3 file csv dan setelah di cek untuk melakukan Content Based Filtering kita cukup menggunakan dataset `anime-dataset-2023` dan untuk Collaborative Filtering kita cukup menggunakan `users-score-2023` yang kemudian akan disimpan kedalam 2 data frame Anime dan Rating.

**Penanganan Missing Value**

- pada tahap Exploratory Data Analysis kita mengidentifikasi terdapat terdapat missing value pada dataset `user-details-2023.csv` pada atribut Username dengan jumlah 1 , Gender berjumlah 506907, Birthday berjumlah 563222, Location berjumlah 578485 dan pada dataset `user-score-2023.csv` missing value berjumlah 232 pada atribut username yang harus dihapus.

    `user_detail.dropna()`

    `user_rating.dropna()`

    total data setelah menghapus missig value pada kedua dataset seperti table berikut:

    | Nama Dataset          | Jumah Baris | Jumlah Kolom |
    | --------------------- | ----------- | ------------ |
    | user-details-2023.csv | 731290      | 16           |

        <br>

    | Nama Dataset        | Jumah Baris | Jumlah Kolom |
    | ------------------- | ----------- | ------------ |
    | user-score-2023.csv | 24325191    | 5            |

**Hapus beberapa atribut yang tidak terlalu penting pada dataframe Rating**

`Rating = user_rating.drop(columns=['Anime Title', 'Username'])`

**Menyamakan Anime Genres**

| anime_id | Name                                              | Genres  |
| -------- | ------------------------------------------------- | ------- |
| 485      | Mahou no Princess Minky Momo                      | UNKNOWN |
| 603      | Hikaru no Go: Hokuto Hai e no Michi               | UNKNOWN |
| 894      | Shinshaku Sengoku Eiyuu Densetsu: Sanada Juu Y... | UNKNOWN |
| 1096     | Nitaboh                                           | UNKNOWN |
| 1115     | Ame to Shoujo to Watashi no Tegami                | UNKNOWN |
| ...      | ...                                               | ...     |
| 24528    | Shayou (Music)                                    | UNKNOWN |
| 24549    | Telepath                                          | UNKNOWN |
| 24635    | Slash                                             | UNKNOWN |
| 24729    | The IDOLM@STER Cinderella Girls: U149 Recap       | UNKNOWN |
| 24856    | Fins                                              | UNKNOWN |

Karena setelah dicek terdapat value `UNKNOWN` pada atribut Genre maka akan kita hapus.

Karena dataframe Rating sangat banyak dan tidak sepadan dengan sumber daya yang saya miliki oleh karena itu kita akan mengambil beberap puluh ribu saja untuk dijadikan sample.

**Mengapa diperlukan tahapan Data Preprocessing?**

- Data preprocessing adalah tahap penting dalam analisis data dan pengembangan model machine learning, yang bertujuan untuk mempersiapkan data agar lebih bersih, relevan, dan siap digunakan. Tahapan ini diperlukan untuk mengurangi kebisingan (noise) dengan menghapus atribut yang tidak penting, seperti yang dilakukan pada dataframe Anime dan Rating, serta meningkatkan kualitas data dengan menghapus nilai yang tidak valid atau 'UNKNOWN' dalam atribut Genre. Selain itu, preprocessing mempercepat proses analisis dengan mengurangi jumlah data dan atribut yang tidak perlu, serta memudahkan pemrosesan data yang lebih terstruktur. Hal ini juga berkontribusi pada peningkatan kinerja model, karena model membutuhkan data yang bersih dan relevan untuk menghasilkan prediksi yang akurat. Dengan demikian, data preprocessing menyediakan basis yang solid untuk analisis lebih lanjut, memastikan bahwa data yang digunakan berkualitas tinggi dan mudah diolah.

### TF-IDF Vectorizer Data Anime

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image.png?raw=true)

- Mengubah data kedalam representasi numerik dengan TF-IDF Vectorizer sebelum tahap Modeling **Cosine Similiarity**

**Mengapa diperlukan Mengubah data kedalam representasi numerik?**

- Data perlu diubah kedalam representasi numerik karena sistem rekomendasi berbasis konten membutuhkan representasi numerik dari teks atau fitur kategori agar dapat mengukur kemiripan antar-item. Misalnya, dalam rekomendasi film, kategori seperti "Action," "Drama," atau "Fantasy" diubah menjadi nilai numerik untuk dihitung kemiripannya.

### Encoding Data User Rating

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-1.png?raw=true)

- Encoding data untuk sebelum tahap pemodelan **Collaborative Filtering**

**Mengapa diperlukan melakukan Encoding data?**

- Encoding data perlu dilakukan karena pada Collaborative Filtering, model harus belajar dari pola interaksi pengguna terhadap item. Data perlu diubah ke dalam bentuk numerik agar model neural network dapat memprosesnya.

### Train-test-split User Rating

Selanjutnya, dilakukan train-test-split dengan pembagian data sebesar 80:20 antara data latih (train) dan data validasi.

**Mengapa diperlukan melakukan Train-test-split data?**

- Memisahkan data menjadi set pelatihan dan pengujian memungkinkan kita untuk mengevaluasi kinerja model pada data yang tidak pernah dilihat sebelumnya. Ini memberikan gambaran yang lebih akurat tentang seberapa baik model yg kita buat.

## Modeling

Pada tahapan model yang digunakan terdiri dari:

- Cosine Similarity
- RecomenderNet

### 1. Cosine Similarity

- **Cara Membuat Model**:

    1. `from sklearn.metrics.pairwise import cosine_similarity`

        - Mengimpor fungsi cosine_similarity dari modul sklearn.metrics.pairwise. Fungsi ini digunakan untuk menghitung kemiripan kosinus antar-vektor (contohnya, antar-vektor TF-IDF yang mewakili deskripsi atau genre anime).

    2. `cosine_sim = cosine_similarity(tfidf_matrix)`

        - Fungsi cosine_similarity menghitung kemiripan kosinus antara semua pasangan baris dalam matriks tfidf_matrix.

    3. `cosine_sim = cosine_similarity(tfidf_matrix)`

        - Fungsi cosine_similarity menghitung kemiripan kosinus antara semua pasangan baris dalam matriks tfidf_matrix.

        - **Penjelasan Parameter**:

            - tfidf_matrix: Matriks yang berisi nilai TF-IDF untuk masing-masing anime.

    ![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-2.png?raw=true)

    pada kode di atas, dengan menggunakan argpartition, kita mengambil sejumlah nilai k tertinggi dari similarity data (dalam kasus ini: dataframe cosine_sim_df). Kemudian, kita mengambil data dari bobot (tingkat kesamaan) tertinggi ke terendah. Data ini dimasukkan ke dalam variabel closest. Berikutnya, kita perlu menghapus nama_anime yang yang dicari agar tidak muncul dalam daftar rekomendasi. Dalam kasus ini, nanti kita akan mencari anime yang mirip dengan Tarareba, sehingga kita perlu drop nama_anime Tarareba agar tidak muncul dalam daftar rekomendasi yang diberikan nanti.

- **Cara Kerja Pendekatan Content-based filtering:**

    Content-based filtering mempelajari profil minat pengguna baru berdasarkan data dari objek yang telah dinilai pengguna. Algoritma ini bekerja dengan menyarankan item serupa yang pernah disukai di masa lalu atau sedang dilihat di masa kini kepada pengguna. Semakin banyak informasi yang diberikan pengguna, semakin baik akurasi sistem rekomendasi.

  - **Kelebihan:**

    - Tidak Bergantung pada Data Pengguna Lain: Hanya membutuhkan data dari item yang direkomendasikan, bukan dari perilaku pengguna lainnya.
    - Personalisasi Berdasarkan Minat Pengguna: Memberikan rekomendasi berdasarkan profil pengguna atau riwayat preferensinya.
    - Efektif untuk Pengguna Baru: Content-based filtering efektif untuk pengguna baru yang belum memiliki riwayat interaksi, selama ada cukup informasi tentang konten.

  - **Kekurangan:**

    - Keterbatasan dalam Diversifikasi: Cenderung merekomendasikan item yang serupa dengan yang sudah disukai pengguna, yang bisa membuat rekomendasi menjadi monoton.
    - Ketergantungan pada Kualitas Fitur Konten: Jika fitur atau deskripsi konten terbatas atau kurang informatif, sistem akan sulit memberikan rekomendasi yang relevan.
    - Tidak Memanfaatkan Informasi dari Pengguna Lain: Sistem ini tidak belajar dari interaksi atau preferensi pengguna lain, yang dapat mengurangi variasi rekomendasi.

- **Cara Kerja Model Cosine Similiarity:**

    Cosine similarity adalah teknik yang digunakan untuk mengukur seberapa mirip dua vektor, terlepas dari ukuran atau panjang vektor tersebut. Pendekatan ini banyak digunakan dalam rekomendasi berbasis konten untuk menilai kesamaan antara dua item (seperti film atau buku) berdasarkan fitur-fitur atau kata kunci yang mereka miliki.

  - **Kelebihan**

    - Independensi Magnitudo: Mengukur kesamaan berdasarkan sudut antara vektor, bukan panjangnya, sehingga efektif untuk data berdimensi tinggi.
    - Efisiensi Komputasi: Perhitungan cepat dan sederhana, ideal untuk dataset besar.

  - **Kekurangan**

    - Mengabaikan Magnitudo: Tidak mempertimbangkan ukuran vektor, yang mungkin relevan dalam beberapa konteks.
    - Sensitif terhadap Noise: Hasil dapat terpengaruh oleh fitur yang tidak relevan atau bising.

### 2. RecomenderNet

- **Cara Membuat Model**:

    1. `import tensorflow as tflw`

        - Mengimpor pustaka TensorFlow dan memberi nama alias tflw.

    2. `from tensorflow import keras`

        - Mengimpor sub-pustaka Keras dari TensorFlow.

    3. `from tensorflow.keras import layers`

        - Mengimpor modul layers dari Keras yang ada di dalam TensorFlow.

    ![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-3.png?raw=true)

    membuat class RecommenderNet dengan keras Model class. Kode class RecommenderNet ini terinspirasi dari tutorial dalam situs Keras dengan beberapa adaptasi sesuai kasus yang ingin diselesaikan.

- **Cara Kerja Pendekatan Collaborative Filtering:**

    Collaborative filtering menganalisis interaksi pengguna dengan item untuk memberikan rekomendasi. Algoritma ini bekerja dengan mencari pola dalam penilaian atau perilaku pengguna dan menyarankan item yang mungkin disukai berdasarkan preferensi pengguna lain yang memiliki kesamaan. Ada dua jenis utama dalam collaborative filtering: user-based yang mencocokkan pengguna serupa, dan item-based yang mencocokkan item yang sering dinilai tinggi oleh pengguna yang sama. Semakin banyak interaksi yang diperoleh, semakin baik akurasi sistem rekomendasi

  - **Kelebihan:**

    - Rekomendasi yang Personalisasi: Memberikan rekomendasi berdasarkan interaksi nyata pengguna, sehingga lebih sesuai dengan preferensi individu.
    - Independen dari Konten: Tidak memerlukan pengetahuan mendalam tentang konten item, sehingga dapat digunakan untuk berbagai jenis item (film, buku, produk, dll).
    - Mendapatkan Rekomendasi Baru: Dapat merekomendasikan item yang tidak dikenal sebelumnya oleh pengguna, membuka kesempatan untuk penemuan baru.

  - **Kekurangan:**

    - Cold Start Problem: Sulit memberikan rekomendasi yang akurat untuk pengguna baru atau item baru yang belum memiliki cukup interaksi.
    - Data Sparsity: Jika data interaksi pengguna sangat sedikit, sulit untuk menemukan pola yang cukup untuk menghasilkan rekomendasi yang baik.
    - Bias terhadap Popularitas: Cenderung merekomendasikan item yang sudah populer, sehingga item yang kurang dikenal bisa terabaikan meskipun mungkin relevan untuk pengguna tertentu.

- **Cara Kerja Model RecommenderNet:**

    RecommenderNet adalah model yang dirancang untuk memberikan rekomendasi kepada pengguna berdasarkan interaksi mereka dengan item sebelumnya. Model ini menggunakan teknik pembelajaran mendalam untuk mempelajari pola dan preferensi pengguna dari data historis. Proses ini melibatkan pengkodean informasi pengguna dan item ke dalam representasi vektor, yang kemudian digunakan untuk memprediksi preferensi pengguna terhadap item yang belum mereka lihat.

  - **Kelebihan**

    - Personalisasi Tinggi: Mampu menghasilkan rekomendasi yang sangat sesuai dengan preferensi individu pengguna berdasarkan analisis data historis.
    - Kemampuan Menangkap Hubungan Kompleks: Dapat memahami dan memodelkan interaksi non-linear antara pengguna dan item, meningkatkan akurasi rekomendasi.

  - **Kekurangan**
    - Memerlukan Banyak Data: Kinerja optimal tergantung pada ketersediaan data yang cukup banyak dan beragam dari pengguna dan item.
    - Kompleksitas Model: Lebih rumit dalam hal arsitektur dan pelatihan dibandingkan metode rekomendasi tradisional, memerlukan lebih banyak sumber daya komputasi.

### Hasil Top-N Rekomendasi Model Cosine Similiarity

| anime_id | Name            | Genres                 |
| -------- | --------------- | ---------------------- |
| 12335    | Hajimete no Gal | Comedy, Romance, Ecchi |

| No  | Name                                              | Genres                 |
| --- | ------------------------------------------------- | ---------------------- |
| 0   | High School DxD New: Oppai, Tsutsumimasu!         | Comedy, Romance, Ecchi |
| 1   | Love Hina Final Selection                         | Comedy, Romance, Ecchi |
| 2   | Mujaki no Rakuen                                  | Comedy, Romance, Ecchi |
| 3   | 1+2=Paradise                                      | Comedy, Romance, Ecchi |
| 4   | Kimi ga Aruji de Shitsuji ga Ore de               | Comedy, Romance, Ecchi |
| 5   | Gift: Eternal Rainbow - Ki no Saka Ryokan Kiki... | Comedy, Romance, Ecchi |
| 6   | Maji de Watashi ni Koi Shinasai!                  | Comedy, Romance, Ecchi |
| 7   | Dakara Boku wa, H ga Dekinai. Mie Sugi! Mizugi... | Comedy, Romance, Ecchi |
| 8   | Sprite: Between Two Worlds                        | Comedy, Romance, Ecchi |
| 9   | Megami no Café Terrace                            | Comedy, Romance, Ecchi |

Berdasarkan hasil tabel di atas model `Cosine Similiarity` berhasil merekomendasikan Top-N anime dengan genre yang sama dengan anime Hajimete no Gal.

### Hasil Top-N Rekomendasi RecommenderNet

<br>

=============================================

**Menampilkan Rekomendasi untuk Pengguna: 707343**

=============================================

**Anime dengan Rating Tertinggi dari Pengguna**

=============================================

| Judul Anime   | Genre  |
| ------------- | ------ |
| **New Game!** | Comedy |

=============================================

**Rekomendasi 10 Anime Teratas**

=============================================

| No. | Judul Anime                                                   | Genre                              |
| --- | ------------------------------------------------------------- | ---------------------------------- |
| 1   | **s.CRY.ed**                                                  | Action, Adventure, Drama, Sci-Fi   |
| 2   | **Slam Dunk**                                                 | Sports                             |
| 3   | **Tactics**                                                   | Mystery, Supernatural              |
| 4   | **One Piece Film: Strong World**                              | Action, Adventure, Fantasy         |
| 5   | **Major S5**                                                  | Sports                             |
| 6   | **Naruto: Shippuuden Movie 3 - Hi no Ishi wo Tsugu Mono**     | Action, Adventure, Fantasy         |
| 7   | **Tegamibachi Reverse**                                       | Adventure, Fantasy                 |
| 8   | **Natsume Yuujinchou San**                                    | Drama, Slice of Life, Supernatural |
| 9   | **Haikyuu!! Karasuno Koukou vs. Shiratorizawa Gakuen Koukou** | Sports                             |
| 10  | **Bocchi the Rock!**                                          | Comedy                             |

Berdasarkan hasil tabel di atas model `RecommenderNet` berhasil merekomendasikan anime dengan rating tertinggi dari pengguna dan merekomendasikan Top-N anime teratas pada Pengguna: 707343.

## Evaluation

Pada project ini ada 2 matrix yang digunakan untuk mengevaluasi model yaitu _Precision_ dan _RMSE (Root Mean Squared Error)_ dengan penjelasan seeperti berikut:

### Evaluasi Model _Cosine Similiarity_

Model ini hanya menggunakan metrik Precision untuk mengetahui seberapa baik perforam model tersebut. Presisi adalah metrik yang biasa digunakan untuk mengevaluasi kinerja model pengelompokan. Metrik ini menghitung rasio antara nilai ground truth (nilai sebenarnya) dengan nilai prediksi yang positf. Perhitungan rasio ini dijabarkan melalui rumus di bawah ini:

$$ Precision = \frac{TP}{TP + FP} $$

Dimana:

- TP (_True Positive_), jumlah kejadian positif yang diprediksi dengan benar.
- FP (_False Positive_), jumlah kejadian positif yang diprediksi dengan salah.

Berdasarkan hasil yang terdapat pada tahap Model and Result dapat dilihat bahwasanya besar presisi jika dihitung adalah 10/10 untuk rekomendasi Top-10. Ini menunjukan sistem mampu memberikan rekomendasi sesuai dengan Genres Animenya.

### Evaluasi Model _RecommenderNet_

Evaluasi metrik yang dapat digunakan untuk mengukur kinerja model ini adalah metrik RMSE (_Root Mean Squared Error_). RMSE adalah metode pengukuran dengan mengukur perbedaan nilai dari prediksi sebuah model sebagai estimasi atas nilai yang diobservasi. RMSE dapat dijabarkan melalui pendekatan rumus berikut ini

$$ RMSE = \sqrt{\frac{\sum\_{t=1}^{n}(A_t - F_t)^2}{n}} $$

Dimana:

- $A_t$ : Nilai aktual
- $F_t$ : Nilai hasil prediksi
- n: Banyak data

_Collaborative Filtering_ dengan model RecommenderNet memberikan hasil training yang divisualisasikan melalui gambar di bawah ini:

![alt text](https://github.com/Agim-dudu/Sistem-Rekomendasi---Anime/blob/main/Resource/image-14.png?raw=true)

Dengan epoch sebanyak 100, model ini memperoleh nilai error akhir sebesar sekitar 0.06 untuk training dan error pada data validasi sebesar 0.25. Nilai tersebut cukup bagus untuk sistem rekomendasi.

Berdasarkan hasil yang didapat pada tahap Model and Result untuk user dengan id 707343 model berhasil merekomendasikan Anime dengan rating tertinggi dari pengguna dan Rekomendasi Top-10 anime teratas untuk user 707343.

## Kesimpulan

Dari hasil evaluasi, solusi sistem rekomendasi dengan pendekatan Content-Based Filtering dengan model Cosine Similarity dan Collaborative Filtering menggunakan model RecommenderNet menunjukkan bahwa kedua pendekatan ini berhasil mencapai tujuan proyek. Content-Based Filtering dengan model Cosine Similiarity memberikan rekomendasi anime yang relevan berdasarkan kesamaan genre dengan presisi tinggi, mencapai rekomendasi Top-10 yang sesuai kategori. Sementara itu, pendekatan Collaborative Filtering dengan model RecommenderNet menghasilkan rekomendasi anime berdasarkan pola rating pengguna dengan error yang rendah (RMSE sekitar 0.06 untuk data training dan 0.25 untuk data validasi), menunjukkan kemampuannya dalam memprediksi preferensi pengguna dengan akurat. Secara keseluruhan, kedua pendekatan ini berhasil memberikan rekomendasi yang relevan dan sesuai dengan tujuan utama, yaitu menyediakan rekomendasi anime yang sesuai dengan preferensi genre dan pola rating pengguna.

## Referensi

1. Mulachela, A., Rizki, K., & Wahyuddin, Y. A. (2020). Analisis Perkembangan Industri Game di Indonesia Melalui Pendekatan Rantai Nilai Global (Global Value Chain). _Indonesian Journal of Global Discourse, 2_(2), 32-51. Retrieved from [Link](https://jtiik.ub.ac.id/index.php/jtiik/article/view/8503).

2. Syamkalla, M. T., Khomsah, S., & Nur, Y. S. R. (2024). Implementasi Algoritma Catboost Dan Shapley Additive Explanations (SHAP) Dalam Memprediksi Popularitas Game Indie Pada Platform Steam. _Jurnal Teknologi Informasi dan Ilmu Komputer, 11_(4), 777-786. Retrieved from [Link](https://ejournal.bsi.ac.id/ejurnal/index.php/ti/article/view/11462).

3. Ricci, F., Rokach, L., & Shapira, B. (2011). Introduction to Recommender Systems Handbook. In _Recommender Systems Handbook_ (pp. 1-35). Springer. Retrieved from [Link](https://link.springer.com/chapter/10.1007/978-0-387-85820-3_1).

4. Resnick, P., Iacovou, N., Suchak, M., Bergstrom, P., & Riedl, J. (1994). GroupLens: An Open Architecture for Collaborative Filtering of Netnews. In _Proceedings of the 1994 ACM Conference on Computer Supported Cooperative Work_ (pp. 175-186). ACM. Retrieved from [Link](https://dl.acm.org/doi/10.1145/192844.192905).

5. Burke, R. (2002). Hybrid Recommender Systems: Survey and Experiments. _User Modeling and User-Adapted Interaction, 12_(4), 331-370. Retrieved from [Link](https://link.springer.com/article/10.1023/A:1021240730564).

<!-- markdownlint-disable MD033 -->
</div>
<!-- markdownlint-enable MD033 -->
