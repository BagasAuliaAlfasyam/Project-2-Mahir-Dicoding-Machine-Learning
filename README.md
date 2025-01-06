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

Output :

`Final jumlah rekomendasi: 41155`

`Final jumlah users: 40771`

Tujuan dari tahap ini adalah memastikan konsistensi dan integritas referensial antara dataset recommendations, users, dan games. Dengan melakukan filtering dan validasi, kita dapat: (1) menghilangkan entri yang tidak valid, (2) memastikan setiap rekomendasi terkait dengan user dan game yang aktual, dan (3) mencegah potensi kesalahan dalam analisis atau pemodelan yang disebabkan oleh data yang tidak konsisten.

#### Cek Konsistensi User ID dan App ID

```python
# Cek Konsistensi User ID dan App ID
missing_users = set(consistent_recommendations['user_id']) - set(sample_data_users['user_id'])
print(f"User ID yang ada di consistent_recommendations tapi tidak ada di users: {len(missing_users)}")

missing_games = set(consistent_recommendations['app_id']) - set(games['app_id'])
print(f"Game ID yang ada di recommendations tapi tidak ada di games: {len(missing_games)}")
```

Output :

`User ID yang ada di consistent_recommendations tapi tidak ada di users: 0`

`Game ID yang ada di recommendations tapi tidak ada di games: 0`

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

Dataset `final_games` dari gabungan dataset `games` dan `games_metadata` yang dari 14 fitur dengan struktur kompleks yang mencakup 4 fitur categorical (title, date_release, rating, description, tags), 6 fitur numerical (app_id, positive_ratio, user_reviews, price_final, price_original, discount), dan 4 fitur boolean untuk platform game (win, mac, linux, steam_deck). Com total 50.872 entri yang memiliki kelengkapan data 100% tanpa missing values, dataset ini menyediakan informasi komprehensif tentang game, termasuk metadata, ulasan pengguna, informasi harga, dan ketersediaan platform, yang memungkinkan analisis mendalam tentang karakteristik dan performa game.

#### `final_games` Statistic Deskriptif

<!-- markdownlint-disable MD033 -->
<div style="overflow-x: auto;">
<!-- markdownlint-enable MD033 -->

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

</div>

Dataset `final_games` menunjukkan variasi signifikan dalam berbagai metrik. app_id memiliki rentang yang luas dari 10 hingga 2,599,300, dengan rata-rata 1,055,224. positive_ratio menunjukkan rata-rata ulasan positif sekitar 77%, dengan standar deviasi 18.25%. Variabel harga (price_final dan price_original) memiliki rata-rata sekitar $8.62, namun dengan rentang yang lebar dari $0 hingga $299.99, menandakan diversitas pricing game.

#### `sample_data_users` Info

| No  | Column           | Non-Null Count  | Dtype   |
| --- | ---------------- | --------------- | ------- |
|  0  | user_id          |  40771 non-null | int32   |
|  1  | products         |  40771 non-null | int32   |
|  2  | reviews          |  40771 non-null | int32   |

Dataset `users` terdiri dari 3 fitur dengan struktur sederhana, mencakup 1 fitur integer (user_id, products, reviews) dengan total 40.771 entri. Total kelengkapan data 100% tanpa missing values, dataset ini memberikan informasi dasar tentang pengguna, fokus pada identifikasi pengguna, jumlah produk, dan jumlah review yang mereka lakukan, yang memungkinkan analisis awal tentang aktivitas dan interaksi pengguna dalam konteks game.

#### `sample_data_users` Statistik Deskriptif

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

Dataset `Users` menggambarkan karakteristik pengguna dengan user_id tersebar dari 519 hingga 14,304,900. Rata-rata jumlah produk per pengguna adalah 274, dengan variasi besar (std 626.77). Jumlah review per pengguna relatif rendah, dengan rata-rata 20.40 review dan median hanya 5 review.

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

#### `sample_recommendations` Statistik Deskriptif
<!-- markdownlint-disable MD033 -->
<div style="overflow-x: auto;">
<!-- markdownlint-enable MD033 -->

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

</div>

3 Table deskriptif diatas memberikan informasi statistik pada masing-masing kolom di 3 dataset, antara lain:

- Count adalah jumlah sampel pada data.
- Mean adalah nilai rata-rata.
- Std adalah standar deviasi.
- Min yaitu nilai minimum setiap kolom.
- 25% adalah kuartil pertama. Kuartil adalah nilai yang menandai batas interval - dalam empat bagian sebaran yang sama.
- 50% adalah kuartil kedua, atau biasa juga disebut median (nilai tengah).
- 75% adalah kuartil ketiga.
- Max adalah nilai maksimum.

### Exploratory Data Analysis - Univariate Analysis

#### 1. Distribusi Platform Game

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar01.png)

Interpretasi data sistem operasi ini mengungkapkan pola penggunaan yang sangat jelas. Windows mendominasi dengan tingkat penetrasi yang hampir mutlak, dengan 98.4% pengguna menggunakan sistem operasi ini, meninggalkan hanya 1.6% untuk sistem operasi lain. Linux menempati posisi ketiga dengan 17.8% pengguna, sementara macOS memiliki pangsa 25.6% pengguna. Hal yang menarik adalah Steam Deck, yang mencatat 100% penggunaan dalam dataset ini, meskipun mungkin memiliki jumlah pengguna yang lebih terbatas. Kesimpulan utama adalah Windows tetap menjadi platform utama dengan keunggulan yang sangat signifikan, sementara macOS dan Linux membentuk segmen minoritas namun tidak diabaikan dalam ekosistem sistem operasi, mencerminkan keanekaragaman pilihan teknologi di kalangan pengguna.

#### 2. Distribusi Rasio Ulasan Positif

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar02.png)

Diagram histogram tersebut menampilkan distribusi rasio ulasan positif dengan cara yang memberikan wawasan mendalam tentang persepsi pengguna. Sumbu horizontal menggambarkan persentase rasio ulasan positif, sementara sumbu vertikal menunjukkan frekuensi kemunculan. Pola distribusi yang terlihat menunjukkan peningkatan bertahap dalam frekuensi seiring naiknya rasio ulasan positif, dengan puncak yang sangat jelas berada pada kisaran 90-100%, di mana lebih dari 15.000 ulasan termasuk dalam kategori ini. Kisaran 70-90% pun memiliki kontribusi yang signifikan dengan sekitar 10.000 ulasan. Sebaliknya, frekuensi ulasan menurun tajam pada rasio di bawah 50%, mengindikasikan bahwa ulasan dengan sentiment negatif sangat jarang terjadi. Kesimpulan yang dapat ditarik adalah bahwa produk atau layanan yang dianalisis sangat positif diterima oleh pengguna, dengan mayoritas ulasan menunjukkan tingkat kepuasan yang tinggi dan konsisten.

#### 3. Distribusi Rating Game

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar03.png)

Diagram batang tersebut menggambarkan distribusi rating game yang menunjukkan pola menarik dalam ulasan pengguna. Kategori **Positive**, **Very Positive**, dan **Mixed** mendominasi dengan frekuensi sekitar 13.000 hingga 14.000 ulasan, mengindikasikan bahwa mayoritas game menerima tanggapan yang cukup baik atau setidaknya beragam. **Mostly Positive** turut menyumbang sekitar 8.000 ulasan, semakin memperkuat kecenderungan ulasan yang relatif positif. Sebaliknya, kategori dengan rating rendah seperti **Mostly Negative**, **Negative**, **Very Negative**, dan **Overwhelmingly Negative** memiliki frekuensi yang jauh lebih sedikit. Kesimpulan yang dapat ditarik adalah bahwa pengalaman pengguna dengan game secara umum cenderung positif, dengan variasi pendapat yang ada, sementara ulasan ekstrem baik yang sangat positif maupun sangat negatif hanya mencakup proporsi kecil dari keseluruhan ulasan.

#### 4. Distribusi Diskon

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar04.png)

Histogram tersebut menunjukkan distribusi persentase diskon. Mayoritas data terpusat di sekitar nilai 0%, yang mengindikasikan bahwa sebagian besar produk atau transaksi tidak mendapatkan diskon. Frekuensi diskon yang lebih tinggi pada nilai rendah (mendekati 0%) secara signifikan menonjol dibandingkan nilai diskon yang lebih tinggi.

Diskon dengan persentase lebih besar dari 20% hingga mendekati 80% jarang terjadi, terlihat dari jumlah bar yang kecil di kisaran tersebut. Distribusi ini mencerminkan bahwa diskon besar lebih jarang diberikan dibandingkan diskon kecil atau tanpa diskon sama sekali.

Hal ini dapat mengindikasikan strategi pemasaran yang lebih sering menawarkan harga penuh atau diskon minimal, dengan hanya sedikit transaksi yang menawarkan diskon besar sebagai insentif tambahan.

#### 5. Distribusi Top 15 Tag Game

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar05.png)

Berdasarkan bar chart yang menampilkan 15 tag game terpopuler, terlihat bahwa tag "Indie" mendominasi dengan frekuensi tertinggi, menandakan besarnya peran game indie dalam dataset. Diikuti oleh tag populer lainnya seperti "Singleplayer," "Action," dan "Adventure" yang menunjukkan minat tinggi terhadap game mode pemain tunggal dan genre aksi atau petualangan. Tag seperti "Casual," "Simulation," dan "2D" menempati posisi menengah dengan frekuensi yang signifikan, sementara "Pixel Graphics" berada di posisi terbawah dari 15 tag teratas namun tetap memiliki keberadaan yang berarti. Secara komprehensif, data ini mencerminkan kecenderungan pengguna atau developer dalam menciptakan dan menikmati game-game indie, berpengalaman singleplayer, dengan fokus pada elemen aksi dan petualangan.

#### 6. Distribusi Word Cloud Tags

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar06.png)

Secara keseluruhan, word cloud ini menggambarkan dataset yang didominasi oleh game-game indie, dengan fokus pada elemen cerita yang kaya, akses awal, dan fitur-fitur permainan yang memberikan kebebasan dan pilihan bagi pemain. Genre game yang beragam, mulai dari aksi, RPG, petualangan, hingga simulasi, juga nampak menonjol dalam dataset ini.

#### 7. Distribusi Word Cloud Descriptions

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar07.png)

Secara keseluruhan, word cloud ini menggambarkan kumpulan game yang menekankan pada pengalaman inovatif, eksplorasi, pembangunan, dan tantangan, dengan unsur-unsur naratif, emosional, dan pengembangan karakter yang kuat. Game-game ini tampaknya mencakup berbagai genre dan gaya, dari tradisional hingga modern, serta menawarkan pengalaman bermain yang beragam bagi para pemain.

### Exploratory Data Analysis - Multivariate Analysis

#### 1. Distribusi Kolom `is_recommended` dan `hours`

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar08.png)

Berdasarkan bar chart yang menampilkan rata-rata waktu bermain (average playtime) dalam jam berdasarkan rekomendasi game (is recommended), dapat diinterpretasikan bahwa game yang direkomendasikan (dengan nilai "True") memiliki rata-rata waktu bermain yang lebih tinggi dibandingkan game yang tidak direkomendasikan (dengan nilai "False"). Hal ini mengindikasikan bahwa rekomendasi game kemungkinan besar berkorelasi dengan tingkat kepuasan atau keterlibatan pengguna, di mana waktu bermain yang lebih lama dapat menjadi indikator bahwa game tersebut menawarkan pengalaman yang menarik atau gameplay yang memikat bagi pemainnya. Untuk meningkatkan rekomendasi game, developer atau platform dapat mempertimbangkan pola ini untuk mengidentifikasi game-game dengan potensi tinggi dalam meningkatkan keterlibatan dan waktu bermain pemain.

#### 2. Analisis Pengguna dengan Produk dan Ulasan

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar09.png)

1. **Distribusi Jumlah Produk per Pengguna (kiri)**:
   Histogram ini menunjukkan bahwa sebagian besar pengguna hanya berinteraksi dengan sejumlah kecil produk. Mayoritas pengguna berada di kisaran jumlah produk yang sangat rendah, dan jumlah pengguna berkurang drastis seiring bertambahnya jumlah produk yang mereka interaksikan. Ada ekor panjang (long tail) yang menunjukkan bahwa sedikit pengguna memiliki jumlah produk yang sangat tinggi.

2. **Distribusi Jumlah Ulasan per Pengguna (kanan)**:
   Pola serupa terlihat pada distribusi ulasan. Sebagian besar pengguna memberikan sangat sedikit ulasan, dengan jumlah pengguna yang menurun tajam seiring bertambahnya jumlah ulasan yang dibuat. Sama seperti grafik pertama, terdapat ekor panjang yang menunjukkan bahwa hanya sejumlah kecil pengguna yang memberikan ulasan dalam jumlah besar.

Secara keseluruhan, kedua distribusi ini menunjukkan pola yang sangat mirip, dengan sebagian besar aktivitas terkonsentrasi pada sebagian kecil pengguna, dan hanya sedikit pengguna yang sangat aktif dalam hal jumlah produk yang diulas atau jumlah ulasan yang dibuat. Fenomena ini umum dalam data interaksi pengguna, yang sering kali mengikuti distribusi yang tidak merata.

#### 3. Korelasi antara kolom `price_final`, `positive_ratio`, `user_reviews` dan `discount`

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar10.png)

Gambar tersebut menggambarkan hubungan antara beberapa variabel `price_final`, `positive_ratio`, `user_reviews`, dan `discount`. Analisis menunjukkan bahwa sebagian besar variabel tidak memiliki hubungan linear yang signifikan, dengan korelasi mendekati nol. Namun, terdapat hubungan lemah yang signifikan antara `price_final` dan `discount`, di mana harga akhir cenderung menurun jika diskon meningkat, meskipun korelasinya lemah. Hasil ini mengindikasikan bahwa faktor-faktor ini perlu dieksplorasi lebih jauh dengan metode selain regresi linier sederhana.

#### 4. Distribusi Harga dan Rasio Review Positif

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar11.png)

 scatter plot yang menunjukkan hubungan antara Harga (x-axis) dan Rasio Review Positif (y-axis). Analisis menunjukkan bahwa sebagian besar produk memiliki harga rendah di bawah 50, dengan rasio review positif yang beragam, mulai dari 0 hingga 100. Tidak terlihat adanya pola hubungan yang jelas antara harga dan rasio review positif. Pada harga yang lebih tinggi, di atas 100, jumlah produk sangat sedikit, tetapi rasio review positif tetap beragam. Hal ini mengindikasikan bahwa produk dengan rasio review positif tinggi tidak terbatas pada kategori harga tertentu. Scatter plot ini bermanfaat untuk mengidentifikasi pola hubungan atau outlier yang membutuhkan perhatian lebih lanjut dalam analisis.

#### 5. Distribusi Harga game berdasarkan seluruh platform

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar12.png)

Berdasarkan diagram ini, dapat dilihat bahwa sebagian besar harga game untuk semua platform berada dalam rentang yang mirip, dengan median harga yang relatif sama. Ada beberapa outlier dengan harga yang jauh lebih tinggi dari kebanyakan game, terutama pada kisaran harga 100 hingga 300. Distribusi harga game untuk setiap platform tampaknya cukup simetris, tanpa perbedaan yang signifikan antara platform yang satu dengan yang lain. Dari segi variabilitas, semua platform memiliki rentang harga yang hampir serupa, menunjukkan bahwa tidak ada platform yang secara signifikan lebih mahal atau lebih murah dibandingkan yang lain.

Secara keseluruhan, diagram ini menunjukkan bahwa harga game cukup konsisten di semua platform, meskipun ada beberapa game yang memiliki harga jauh lebih tinggi yang dianggap sebagai outlier.

#### 6. Distribusi Diskon dan Harga

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar13.png)

diagram ini menunjukkan bahwa meskipun ada berbagai tingkat diskon yang diterapkan, game-game dengan harga lebih tinggi cenderung memiliki diskon yang lebih kecil. Sementara game dengan harga lebih rendah lebih mungkin mendapatkan diskon yang lebih besar. Hal ini bisa menunjukkan strategi penetapan harga di mana game yang lebih murah diberikan diskon lebih besar untuk menarik lebih banyak pembeli.

#### 7. Distribusi Jumlah Review dan Rasio Positif

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar14.png)

Diagram ini menunjukkan hubungan antara jumlah review pengguna dan rasio review positif. Sebagian besar game memiliki rasio review positif tinggi, terutama di atas 80%, dengan hanya sedikit game yang memiliki rasio di bawah 40%. Kebanyakan game juga memiliki jumlah review yang rendah, dengan beberapa outlier yang memiliki jumlah review sangat tinggi, mencapai lebih dari 1 juta. Tidak ada hubungan yang jelas antara jumlah review dan rasio review positif, karena game dengan review sedikit maupun banyak dapat memiliki rasio positif yang tinggi. Outliers dengan lebih dari 3 juta review umumnya memiliki rasio positif di atas 60%. Secara keseluruhan, diagram ini menunjukkan bahwa banyak game memiliki rasio review positif tinggi terlepas dari jumlah review yang diterima, meskipun ada variabilitas signifikan dalam data.

## Data Preparation

### Content-based Filtering preparation

#### 1. Pemilihan Data

Tahap pemilihan data merupakan fondasi kritis dalam membangun sistem rekomendasi. Proses ini dimulai dengan seleksi kolom yang paling relevan untuk menganalisis karakteristik game. Dengan memilih kolom seperti `app_id`, `title`, `description`, dan `tags`, kita membatasi dataset pada informasi esensial yang akan digunakan untuk memahami keunikan setiap game.

```python
df = final_games[['app_id', 'title','description', 'tags']]
```

Selanjutnya, dilakukan transformasi data dengan menggabungkan tags menjadi string tunggal. Langkah ini penting untuk mempersiapkan data teks guna proses pengolahan selanjutnya. Dengan mengkonversi list tag menjadi string, kita menyederhanakan struktur data dan memudahkan analisis tekstual.

```python
df.loc[:, 'tags'] = df['tags'].apply(lambda x:' '.join(x))
```

Tahap krusial berikutnya adalah pembuatan kolom overview. Di sini, kita mengintegrasikan berbagai informasi deskriptif - judul, deskripsi, dan tags - menjadi satu representasi komprehensif dari setiap game. Pendekatan ini memungkinkan analisis mendalam dengan memanfaatkan seluruh informasi yang tersedia.

```python
df.loc[:, 'overview'] = df['title'] + " " + df['description'] + " " + df['tags']
```

Kita membuat dataframe final dengan menyeleksi kolom-kolom `app_id`, `title`, dan `overview` dari dataframe asli. Kolom app_id berfungsi sebagai identifikasi unik untuk setiap aplikasi, kolom `title` menyimpan judul aplikasi yang menggambarkan nama atau identitas aplikasi tersebut, dan kolom `overview` mengintegrasikan informasi deskriptif yang telah kita buat sebelumnya. Dengan menyatukan judul, deskripsi, dan tags ke dalam kolom `overview`, kita mendapatkan representasi komprehensif dari setiap game yang mencakup berbagai aspek penting. Dataframe ini akan digunakan untuk analisis lebih lanjut, memungkinkan kita memanfaatkan seluruh informasi yang tersedia dalam analisis mendalam dan memberikan wawasan yang lebih baik tentang setiap aplikasi game.

```python
final_df = df[['app_id','title','overview']]
```

#### 2. Preprocessing Teks

Preprocessing teks adalah tahap transformasi data mentah menjadi format yang lebih terstruktur dan siap untuk dianalisis. Tahap ini sangat penting untuk memastikan data teks yang digunakan dalam analisis bebas dari elemen-elemen yang dapat mengganggu, seperti tanda baca, karakter khusus, dan simbol-simbol lain yang tidak relevan. Salah satu langkah kunci dalam preprocessing teks adalah pembersihan karakter khusus. Proses ini bertujuan untuk menghilangkan elemen-elemen yang tidak diperlukan, sehingga teks menjadi lebih bersih dan mudah dianalisis. Dengan melakukan pembersihan karakter khusus, kita dapat meningkatkan akurasi model analisis teks dan memastikan bahwa hasil analisis lebih dapat diandalkan.

Berikut adalah fungsi yang digunakan untuk menghapus karakter khusus dari teks:

```python
def remove_special_characters(s):
  return re.sub(r'[^\w\s]', '', s)
```

Fungsi `remove_special_characters` menggunakan ekspresi reguler untuk menghapus semua karakter yang bukan huruf, angka, atau spasi dari string yang diberikan. Ini memastikan bahwa teks hanya terdiri dari kata-kata dan angka yang relevan untuk analisis.

Menerapkan pembersihan karakter khusus pada kolom `overview`:

```python
df['overview'] = df['overview'].apply(lambda x : remove_special_characters(x))
```

Dalam langkah ini, kita menerapkan fungsi `remove_special_characters` ke setiap elemen di kolom `overview` dengan menggunakan metode `apply` dan `lambda`. Hasilnya adalah kolom `overview` yang telah dibersihkan dari karakter-karakter khusus, sehingga teks lebih terstruktur dan siap untuk dianalisis lebih lanjut.

Manfaat dari tahap ini meliputi:

1. **Meningkatkan Kualitas Data:** Menghilangkan karakter yang tidak relevan membuat data lebih bersih dan berkualitas tinggi.
2. **Meningkatkan Akurasi Analisis:** Dengan data yang bersih, model analisis teks dapat bekerja lebih baik dan memberikan hasil yang lebih akurat.
3. **Mudah Diproses:** Teks yang telah diproses lebih mudah untuk dianalisis dan diproses lebih lanjut dalam tahap-tahap berikutnya.
4. **Memperbaiki Kinerja Model:** Model machine learning dan analisis teks dapat berjalan lebih efisien dan efektif dengan data yang telah diproses dengan baik.

#### 3. Stemming Teks

Stemming merupakan teknik penting dalam pengolahan bahasa alami yang mengubah kata ke bentuk dasarnya. Ini mengurangi variasi linguistik dan menyederhanakan analisis. Dengan menggunakan Porter Stemmer, kita dapat mengelompokkan kata-kata yang memiliki akar yang sama.

Berikut adalah implementasi fungsi stemming menggunakan Porter Stemmer:

```python
ps = PorterStemmer()

def stem(text):
    return " ".join([ps.stem(word) for word in text.split()])
```

Fungsi `stem` ini memecah teks menjadi kata-kata terpisah, menerapkan stemming pada setiap kata, dan kemudian menggabungkannya kembali menjadi sebuah kalimat.

Selanjutnya, kita menerapkan stemming pada kolom `overview`:

```python
df['overview'] = df['overview'].apply(stem)
```

Penerapan ini memastikan bahwa setiap kata dalam kolom `overview` diubah ke bentuk dasarnya, membantu mengurangi variasi kata dan menyederhanakan analisis selanjutnya. Manfaatnya termasuk meningkatkan konsistensi data dan efisiensi dalam proses analisis teks.

#### 4. Vektorisasi Teks dan Similarity

Vektorisasi adalah proses mengubah teks menjadi representasi numerik yang dapat dianalisis menggunakan metode komputasi. Count Vectorizer digunakan untuk mengkonversi teks menjadi vektor, dengan pembatasan fitur untuk efisiensi komputasi.

Berikut adalah langkah-langkah untuk melakukan vektorisasi dan menghitung kesamaan (similarity):

**1. Inisialisasi Count Vectorizer:**

```python
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer(max_features=1500, stop_words='english')
```

**2. Mengubah teks menjadi vektor numerik:**

```python
vectors = cv.fit_transform(df['overview']).toarray()
```

**3. Menghitung kesamaan kosinus:**

```python
from sklearn.metrics.pairwise import cosine_similarity
similarity = cosine_similarity(vectors)
```

Dalam proses ini, teks diubah menjadi vektor numerik menggunakan Count Vectorizer, yang membatasi jumlah fitur hingga 1500 dan mengabaikan stop words dalam bahasa Inggris. Setelah itu, vektor numerik tersebut digunakan untuk menghitung kesamaan antar teks menggunakan metrik kesamaan kosinus. Hal ini memungkinkan kita untuk mengukur seberapa mirip teks satu dengan yang lainnya, yang sangat berguna dalam berbagai analisis teks seperti clustering dan rekomendasi.

----------------------------------------------------------------

### Collaborative Filtering Preparation

#### 1. Persiapan Matriks Rekomendasi User-Games

Pada tahap ini, kita membuat matriks yang menunjukkan hubungan antara pengguna dan game. Setiap sel dalam matriks berisi **1** jika game direkomendasikan untuk pengguna tersebut, dan **0** jika tidak. Metode `pivot_table()` digunakan untuk mengubah data mentah menjadi format matriks yang dapat dianalisis.

Berikut implementasinya:

```python
# Membuat matriks pivot yang menghubungkan user dengan game yang direkomendasikan
user_item_matrix = sample_recommendations.pivot_table(
    index='user_id',
    columns='app_id',
    values='is_recommended',
    aggfunc='first'
).fillna(0)
```

#### 2. Menghitung Kesamaan Antar Pengguna

Pada tahap ini, kita menghitung kesamaan antara pengguna menggunakan **cosine similarity**. Metode ini mengukur kosinus sudut antara vektor preferensi game setiap pengguna. Semakin dekat nilai kosinus sudutnya ke **1**, semakin mirip preferensi game antara dua pengguna.

Berikut implementasinya:

```python
# Menghitung cosine similarity antar user
user_similarity = cosine_similarity(user_item_matrix)
user_similarity_df = pd.DataFrame(
    user_similarity,
    index=user_item_matrix.index,
    columns=user_item_matrix.index
)
```

Tujuannya di sini adalah untuk mengidentifikasi pengguna dengan selera game yang serupa. Dengan menggunakan kesamaan kosinus, sistem:

- Mengukur "sudut" antara vektor preferensi pengguna.
- Menentukan seberapa dekat preferensi game dua pengguna selaras.
- Memungkinkan menemukan pengguna "serupa" yang mungkin menikmati jenis game yang sama.

Bayangkan ini seperti menemukan teman dengan daftar putar musik yang hampir identik - jika dua pengguna menyukai game yang sangat mirip, mereka cenderung menikmati rekomendasi tambahan dari riwayat permainan satu sama lain.

#### 3. Persiapan Matriks Rekomendasi Games-Games

Serupa dengan matriks user-game, tetapi kali ini kita membalik perspektif: sekarang matriks menghubungkan game dengan pengguna yang merekomendasikannya.

Berikut implementasinya:

```python
# Buat matriks item-item
item_item_matrix = sample_recommendations.pivot_table(
    index='app_id',
    columns='user_id',
    values='is_recommended',
    aggfunc='first'
).fillna(0)
```

Matriks ini memungkinkan analisis hubungan antar game. Perspektif ini berguna untuk memahami apakah ada game yang memiliki pola rekomendasi serupa di antara pengguna.

#### 4. Menghitung Kesamaan Antar Game

Tahap ini menghitung kesamaan antar game menggunakan **cosine similarity**, mirip dengan perhitungan kesamaan antar pengguna sebelumnya.

Berikut implementasinya:

```python
# Menghitung cosine similarity antar game
item_similarity = cosine_similarity(item_item_matrix)
item_similarity_df = pd.DataFrame(
    item_similarity,
    index=item_item_matrix.index,
    columns=item_item_matrix.index
)
```

----------------------------------------------------------------

### Hybrid Recommendation System preparation

#### 1. Konversi Tags ke Format List

Langkah pertama adalah mengonversi tipe data `tags` dari tuple menjadi list menggunakan `final_games['tags_list'] = final_games['tags'].apply(list)`. Ini dilakukan agar format data lebih mudah diolah dengan `MultiLabelBinarizer` untuk representasi fitur kategori.

#### 2. One-Hot Encoding pada Tags

Selanjutnya, dilakukan proses one-hot encoding pada kolom `tags_list` menggunakan `MultiLabelBinarizer`. Proses ini menghasilkan representasi binary untuk setiap tag, sehingga model dapat memahami hubungan antar kategori secara numerik.

#### 3. Tokenisasi dan Padding Deskripsi

Deskripsi game kemudian diubah menjadi format numerik melalui tokenisasi menggunakan `Tokenizer`. Teks deskripsi diubah menjadi urutan angka dengan `tokenizer.texts_to_sequences`, dan panjang sekuen diseragamkan menggunakan `pad_sequences` dengan panjang maksimum 200. Hal ini memastikan konsistensi input model.

#### 4. Normalisasi Harga

Harga game dinormalisasi menggunakan layer `Normalization`. Nilai harga diadaptasi terlebih dahulu dengan `price_normalizer.adapt`, kemudian dinormalisasi agar skala fitur tidak mendominasi selama proses pelatihan.

#### 5. Normalisasi Positive Ratio

Positive ratio dinormalisasi dengan membaginya dengan 100, sehingga nilainya berada dalam rentang [0,1] untuk selaras dengan fungsi aktivasi sigmoid yang digunakan di output.

#### 6. Representasi Dukungan Platform

Dukungan platform (Windows, Mac, Linux, Steam Deck) direpresentasikan sebagai fitur binary. Kolom ini langsung diambil dari dataset menggunakan `final_games[['windows', 'mac', 'linux', 'steam_deck']].values` untuk mempermudah pemrosesan.

#### 7. Pembagian Data Train dan Test

Terakhir, data dibagi menjadi train dan test dengan rasio 80:20 menggunakan `train_test_split`. Fitur yang digunakan meliputi representasi one-hot encoding untuk tags, urutan numerik dari deskripsi, harga yang telah dinormalisasi, dan fitur binary dari platform. Targetnya adalah nilai positive ratio yang telah dinormalisasi.

----------------------------------------------------------------

## Model and Results

### Sistem Rekomendasi Games - Content-based Filtering

Implementasi Fungsi rekomendasi yang merupakan inti dari sistem content-based filtering. Fungsi ini mengambil sebuah game sebagai input, kemudian mencari game-game lain yang memiliki kesamaan konten berdasarkan vektor similaritas yang telah dihitung.

Berikut adalah implementasi fungsi rekomendasi:

```python
def recommend(game):
    # Periksa apakah game ada dalam DataFrame
    if game not in final_df['title'].values:
        print("Game not found in the dataset.")
        return

    # Jika game ada, lanjutkan dengan rekomendasi
    game_index = final_df[final_df['title'] == game].index[0]
    distances = similarity[game_index]
    game_list = sorted(list(enumerate(distances)), reverse=True, key=lambda x: x[1])[1:11]

    for i in game_list:
        print(final_df.iloc[i[0]].title)
```

Fungsi ini pertama-tama memeriksa apakah game yang dimasukkan pengguna ada dalam dataset. Langkah ini penting untuk memastikan bahwa game yang dicari memang tersedia dalam data yang telah kita proses. Jika game tidak ditemukan, fungsi akan menampilkan pesan "Game not found in the dataset." dan menghentikan eksekusi.

Jika game ada dalam dataset, fungsi kemudian menemukan indeks game tersebut dalam DataFrame `final_df`. Indeks ini digunakan untuk mengakses data terkait game yang dimasukkan pengguna, termasuk informasi kesamaannya dengan game-game lain.

Fungsi kemudian mengambil vektor similaritas dari game yang dipilih menggunakan indeks yang ditemukan. Vektor ini berisi nilai kesamaan kosinus antara game yang dipilih dan semua game lainnya dalam dataset. Nilai kesamaan ini dihitung sebelumnya menggunakan metode vektorisasi dan similarity.

Setelah mendapatkan vektor similaritas, fungsi mengurutkan game-game dalam dataset berdasarkan nilai kesamaan tersebut. Pengurutan dilakukan secara menurun, dari yang paling mirip hingga yang kurang mirip. Game yang sama (yang memiliki kesamaan tertinggi dengan dirinya sendiri) diabaikan dengan mengambil urutan mulai dari elemen kedua dalam daftar hasil pengurutan.

Akhirnya, fungsi mencetak judul-judul game yang paling mirip dengan game yang dipilih, sebanyak 10 game teratas. Ini memberikan rekomendasi kepada pengguna tentang game-game lain yang mungkin menarik bagi mereka berdasarkan kesamaan konten dengan game yang dipilih.

```python
recommend('Prince of Persia: Warrior Within™')
```

```cmd
Output:
Prince of Persia®: The Sands of Time
Prince of Persia: The Two Thrones™
Prince of Persia®
Prince of Persia: The Forgotten Sands™
Legacy of Kain: Soul Reaver 2
DARK SOULS™ III - The Ringed City™
BERSERK and the Band of the Hawk
Dark Fantasy Warriors
Dark Cave
Dragon's Dogma: Dark Arisen
```

Akhirnya, fungsi mencetak judul-judul game yang paling mirip dengan game yang dipilih, sebanyak 10 game teratas. Ini memberikan rekomendasi kepada pengguna tentang game-game lain yang mungkin menarik bagi mereka berdasarkan kesamaan konten dengan game yang dipilih.

Dengan implementasi ini, sistem rekomendasi berhasil menyelesaikan permasalahan dengan menyediakan rekomendasi game berdasarkan kesamaan konten, serta menyajikan top-N recommendation sebagai output, yang dalam hal ini adalah 10 game teratas yang paling mirip.

#### Formula Matrix Similarity

***Cosine Similarity***

Cosine similarity digunakan untuk mengukur kesamaan antara dua vektor non-zero dalam ruang multi-dimensi. Dalam konteks sistem rekomendasi game, formula ini membantu menentukan seberapa mirip konten antar game.

$$cos(\theta) = \frac{A \cdot B}{||A|| \times ||B||}$$

Dimana:

- $A \cdot B$ adalah dot product dari vektor A dan B
- $||A||$ adalah magnitude (panjang) vektor A
- $||B||$ adalah magnitude (panjang) vektor B
- $\theta$ adalah sudut antara kedua vektor

**Perhitungan Detail**
$$cos(\theta) = \frac{\sum_{i=1}^{n} A_i \times B_i}{\sqrt{\sum_{i=1}^{n} A_i^2} \times \sqrt{\sum_{i=1}^{n} B_i^2}}$$

Interpretasi Nilai

- Rentang nilai: 0 sampai 1
- 0: Tidak ada kesamaan
- 1: Kesamaan sempurna

Contoh Sederhana

Misal vektor game:

- A = [1, 2, 3]
- B = [2, 3, 4]

$$cos(\theta) = \frac{(1 \times 2) + (2 \times 3) + (3 \times 4)}{\sqrt{1^2 + 2^2 + 3^2} \times \sqrt{2^2 + 3^2 + 4^2}}$$

#### **Implementasi dalam Kode**

```python
from sklearn.metrics.pairwise import cosine_similarity

# Menghitung similarity matrix
similarity_matrix = cosine_similarity(game_vectors)
```

**Kelebihan** **Metode**

- Tidak terpengaruh ukuran vektor
- Fokus pada arah vektor, bukan magnitudo
- Cocok untuk data berdimensi tinggi

**Kekurangan** **Metode**

- Tidak mempertimbangkan konteks semantik
- Sensitif terhadap preprocessing teks

### Sistem Rekomendasi Games - Collaborative Filtering

#### Pengujian Sistem Rekomendasi untuk Pengguna Tertentu

Pada tahap ini, kita mengambil seorang pengguna contoh `(user ID 10317527)`, mencari pengguna-pengguna yang memiliki preferensi serupa, kemudian mengumpulkan game yang direkomendasikan oleh pengguna serupa. Hasilnya adalah 10 game teratas berdasarkan rasio positif.

Berikut Implementasinya

```python
# Memilih contoh user dan mencari game rekomendasi berdasarkan user serupa
example_user_id = 10317527

# Temukan users terdekat
similar_users_indices = similar_users.argsort()[::-1][1:11]

# Kumpulkan game rekomendasi
recommended_games = []
for similar_user_index in similar_users_indices:
    similar_user_id = user_item_matrix.index[similar_user_index]
    similar_user_games = user_item_matrix.loc[similar_user_id]
    recommended_games.extend(
        similar_user_games[similar_user_games == 1].index.tolist()
    )

# Filter dan ranking rekomendasi
user_recommendations = final_games[final_games['app_id'].isin(recommended_games)].sort_values('positive_ratio', ascending=False).head(10)
```

**Output:**

```Output
Recommended games for user 10317527:
                                                   title  positive_ratio
47394                    Plants vs. Zombies GOTY Edition              97
47793                                           Factorio              96
13504                                 Fallout: New Vegas              96
47428  The Elder Scrolls III: Morrowind® Game of the ...              95
48165                                              Noita              95
47500                                       SpeedRunners              94
2620                              Turok 2: Seeds of Evil              93
3372                                       Geometry Dash              93
11280                                        Cave Story+              92
47495                                  Crusader Kings II              90
```

 Sistem mencari pengguna-pengguna dengan preferensi serupa, kemudian mengumpulkan dan meranking game yang direkomendasikan oleh pengguna serupa tersebut terdapat 10 rekomendasi game untuk user `10317527`.

#### Melakukan Pengujian Collaborative Filtering

```python
# Memilih game contoh dan mencari game serupa
example_game_id = final_games['app_id'].iloc[0]
game_index = item_item_matrix.index.get_loc(example_game_id)

# Temukan game terdekat
similar_games_indices = item_similarity[game_index].argsort()[::-1][1:11]
similar_game_ids = item_item_matrix.index[similar_games_indices]

# Filter dan ranking game serupa
similar_games = final_games[final_games['app_id'].isin(similar_game_ids)].sort_values('positive_ratio', ascending=False)
```

Output:

```output
Rekomendasi Game untuk User 10317527
       app_id                                              title  \
47394    3590                    Plants vs. Zombies GOTY Edition
47793  427520                                           Factorio
13504   22380                                 Fallout: New Vegas
47428   22320  The Elder Scrolls III: Morrowind® Game of the ...
48165  881100                                              Noita
47500  207140                                       SpeedRunners
2620   405830                             Turok 2: Seeds of Evil
3372   322170                                      Geometry Dash
11280  200900                                        Cave Story+
47495  203770                                  Crusader Kings II

       positive_ratio
47394              97
47793              96
13504              96
47428              95
48165              95
47500              94
2620               93
3372               93
11280              92
47495              90

Game Serupa dengan Prince of Persia: Warrior Within™
       app_id                         title  positive_ratio
16192  400630     Wuppo: Definitive Edition              95
12101  398850  Epistory - Typing Chronicles              94
3778   399640                    Flamebreak              93
19813  399820     Kopanito All-Stars Soccer              84
14491  399810              Call of Cthulhu®              78
20921  400130                Freedom Poopie              70
13110  400360       Adam's Venture: Origins              66
19362  399120                      Prospekt              62
22268  399420                     The Prism              62
50642  400250        Heaven Island - VR MMO              53
```

Tes akhir menunjukkan dua strategi rekomendasi:

1. Berbasis pengguna yang Merekomendasikan game yang dinikmati pengguna serupa
2. Berbasis item yang Merekomendasikan game yang mirip dengan game tertentu

Misalnya, saat melihat "Prince of Persia: Warrior Within", sistem menemukan 10 game dengan pola rekomendasi pengguna yang serupa. sistem rekomendasi ini seperti versi yang sangat canggih dari "Jika Anda menyukai ini, Anda mungkin juga menyukai...". Ini menggunakan teknik matematika untuk menemukan pola dalam cara pengguna merekomendasikan game, menciptakan mesin rekomendasi yang cerdas dan berbasis data.
Dengan menggabungkan kesamaan pengguna dan kesamaan game, sistem dapat memberikan rekomendasi yang dipersonalisasi yang melampaui pencocokan genre sederhana, dengan mempertimbangkan preferensi pengguna dan karakteristik game yang bernuansa.

#### **Evaluasi Matrix**

Cosine similarity mengukur kesamaan antara dua vektor \( A \) dan \( B \) berdasarkan sudut di antara keduanya. Rumusnya adalah:

$$
\text{cos}(\theta) = \frac{A \cdot B}{\|A\| \cdot \|B\|}
$$

Dimana:

- **Dot product** \( A \cdot B \) dihitung sebagai:
  $$
  A \cdot B = \sum_{i=1}^n (A_i \cdot B_i)
  $$

- **Norma** \( \|A\| \) dari vektor \( A \) dihitung dengan:
  $$
  \|A\| = \sqrt{\sum_{i=1}^n A_i^2}
  $$

- **Norma** \( \|B\| \) dari vektor \( B \):
  $$
  \|B\| = \sqrt{\sum_{i=1}^n B_i^2}
  $$

Sehingga formula lengkap menjadi:
$$
\text{cos}(\theta) = \frac{\sum_{i=1}^n (A_i \cdot B_i)}{\sqrt{\sum_{i=1}^n A_i^2} \cdot \sqrt{\sum_{i=1}^n B_i^2}}
$$

#### **Penerapan pada Matriks Rekomendasi**

Dalam konteks matriks rekomendasi:

1. **Vektor \( A \) dan \( B \):** Representasi preferensi
pengguna atau item.
   - Contoh: Pada matriks **user-item**, \( A \) dapat berupa preferensi pengguna pertama, dan \( B \) adalah preferensi pengguna kedua.
2. **Komponen Matriks:**
   - **User-user similarity:** Kemiripan antar pengguna dihitung dari vektor pengguna pada matriks **user-item**.
   - **Item-item similarity:** Kemiripan antar item dihitung dari vektor item pada matriks **item-item**.
3. **Nilai Vektor:**
   - Biner (\( 0/1 \)) jika hanya menunjukkan ada atau tidak preferensi.
   - Skalar (misalnya rating) jika menunjukkan tingkat preferensi.

#### **Kelebihan dan Kekurangan Matriks Cosine Similarity Gabungan**

#### **Kelebihan**

Cosine similarity memiliki keunggulan yang sangat signifikan dalam sistem rekomendasi. Metode ini mampu mengukur kesamaan antar vektor secara independen dari skala, artinya tidak terpengaruh oleh perbedaan ukuran dataset atau panjang vektor. Ini membuatnya sangat fleksibel dan dapat diaplikasikan pada berbagai jenis data, baik dalam collaborative filtering maupun content-based filtering. Komputasi matematis yang sederhana membuatnya efisien dari segi waktu dan sumber daya komputasi, sementara interpretasi nilainya yang mudah dipahami (antara 0-1) membuatnya dapat dimengerti bahkan oleh non-teknis.

#### **Kekurangan**

Namun, cosine similarity memiliki beberapa keterbatasan penting yang perlu dipertimbangkan. Metode ini hanya mengukur kesamaan matematis secara permukaan, tanpa mampu memahami konteks semantik yang lebih mendalam. Hasilnya, rekomendasi yang dihasilkan mungkin kehilangan nuansa kompleks dalam data. Metode ini sangat sensitif terhadap proses preprocessing, di mana kesalahan kecil dalam transformasi data dapat secara signifikan mempengaruhi hasil akhir. Selain itu, cosine similarity cenderung lemah dalam menangkap hubungan non-linear dan mengalami kesulitan dengan data kategorikal, serta berpotensi menciptakan bias pada dataset yang tidak seimbang.

#### **Solusi dan Pendekatan**

Untuk mengatasi keterbatasan ini, para praktisi umumnya merekomendasikan pendekatan hibrid. Ini bisa dilakukan dengan mengkombinasikan cosine similarity dengan metode lain, menambahkan lapisan semantik yang lebih canggih, atau menggunakan teknik preprocessing yang lebih kompleks. Validasi silang berkala dan pertimbangan metrik evaluasi tambahan juga dapat membantu meningkatkan akurasi dan kehandalan sistem rekomendasi yang menggunakan cosine similarity.

Dengan pemahaman yang mendalam tentang kelebihan dan kekurangan metode ini, pengembang dapat merancang sistem rekomendasi yang lebih cerdas, adaptif, dan memenuhi kebutuhan spesifik dari berbagai jenis dataset dan konteks penggunaan.

### Sistem Rekomendasi Games - Hybrid Recommendation System

#### Sistem Rekomendasi

Model rekomendasi dirancang menggunakan pendekatan hybrid yang memadukan berbagai fitur, yaitu tags, deskripsi, dan platform.

#### Arsitektur Model

Model memiliki tiga input layer: `tags_input` untuk fitur tags, `description_input` untuk fitur deskripsi, dan `platform_input` untuk fitur platform. Layer embedding digunakan untuk mempelajari representasi vektor dari deskripsi game. Dua hidden layers fully connected dengan aktivasi ReLU digunakan, diikuti oleh satu output layer dengan aktivasi sigmoid untuk memprediksi positive_ratio.

#### Training dan Evaluasi

Model dilatih selama 50 epoch dengan batch size 32 menggunakan optimizer Adam, loss Mean Squared Error (MSE), dan metrics Mean Absolute Error (MAE). Hasil evaluasi menunjukkan performa baik dengan error rendah pada data test. Visualisasi grafik Loss dan MAE memperlihatkan tren penurunan yang konsisten selama pelatihan.

![alt text](https://raw.githubusercontent.com/BagasAuliaAlfasyam/Project-2-Mahir-Dicoding-Machine-Learning/refs/heads/main/gambar/gambar15.png)

#### Output Top-N Recommendation

Model digunakan untuk memprediksi positive_ratio pada 10 sampel game. Hasil prediksi ditampilkan dalam bentuk persentase untuk membantu pengguna memilih game terbaik berdasarkan prediksi model.

```output
                                                   title  predicted_rating
49826                                          Sole Saga         86.379143
1360   Forza Horizon 4:  1977 Hoonigan Ford Gymkhana ...         79.322044
29237                                        Exile's End         67.646233
49474                    Realm Royale - Bass Drop Bundle         73.620468
20970                             Pixel Puzzles: UndeadZ         69.672562
48563                             X4: Cradle of Humanity         65.723648
28220                                   Dungeons Forever         87.861725
28095   Train Simulator: LNER Raven Q6 Steam Loco Add-On         67.258919
4074             Euro Truck Simulator 2 - Viking Legends         82.841743
3264                                       Find Yourself         84.825981
```

#### Pendekatan Alternatif

Pendekatan pertama adalah content-based filtering, yang menggunakan informasi fitur konten untuk memberikan rekomendasi. Kelebihannya adalah tidak memerlukan data pengguna, namun kelemahannya adalah rentan terhadap cold start untuk konten baru. Pendekatan kedua adalah collaborative filtering, yang menggunakan data interaksi pengguna untuk menghasilkan rekomendasi yang lebih personal. Kelebihannya adalah dapat memberikan rekomendasi yang relevan berdasarkan preferensi pengguna lain, namun kekurangannya adalah rentan terhadap cold start untuk pengguna baru.

#### Formula Matrix

Model dilatih menggunakan fungsi *loss* Mean Squared Error (MSE):

$$
MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$

Dengan optimasi dilakukan menggunakan algoritma Adam.  

Hasil evaluasi menunjukkan rata-rata kesalahan absolut (*Mean Absolute Error* atau MAE) sebagai berikut:

$$
MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
$$

#### Kesimpulan - rekomendasi hybrid

1. Kelebihan

   - Pendekatan Hybrid Dengan menggabungkan berbagai fitur (tags, deskripsi, dan platform), model dapat menghasilkan rekomendasi yang lebih relevan.
   - Efisiensi Representasi Teks Penggunaan embedding layer memungkinkan model mempelajari representasi yang kaya dari deskripsi game.
   - Normalisasi Data harga dan positive ratio meningkatkan stabilitas pelatihan.

2. Kekurangan

   - Kompleksitas Model Dengan banyaknya input dan layer, waktu pelatihan dan inferensi menjadi lebih lama dibandingkan pendekatan sederhana.
   - Overfitting Model dengan banyak parameter memiliki risiko overfitting pada data latih jika tidak diatur dengan baik.
   - Ketergantungan pada Data Tags Jika data tags tidak lengkap atau tidak relevan, rekomendasi model bisa menurun kualitasnya.

Model rekomendasi hybrid berhasil memadukan berbagai fitur untuk memberikan prediksi positive_ratio yang akurat. Dua pendekatan alternatif dapat digunakan tergantung kebutuhan, dengan kelebihan dan kekurangan masing-masing.

## Evaluation

### **Content-Based Filtering**

Pada sistem berbasis konten, rekomendasi diberikan berdasarkan kesamaan tag antara game target, *Prince of Persia: Warrior Within™*, dengan game lainnya. Evaluasi menunjukkan bahwa **Precision@10** mencapai nilai **0.700**, yang berarti 70% dari 10 rekomendasi teratas relevan dengan game target. Hal ini mencerminkan kualitas yang baik dalam menyaring game dengan kesamaan yang tinggi.

Selain itu, metrik **NDCG@10** atau *Normalized Discounted Cumulative Gain* menghasilkan nilai **0.992**, yang hampir mendekati sempurna. NDCG mengukur kualitas urutan rekomendasi, menunjukkan bahwa game yang lebih relevan ditempatkan di posisi lebih tinggi dalam daftar rekomendasi. Perhitungan NDCG dilakukan dengan membandingkan relevansi aktual setiap rekomendasi dengan relevansi terbaik yang mungkin dicapai (ideal ranking).

Kode yang digunakan untuk menghitung Precision@10 menghitung jumlah rekomendasi yang memiliki kesamaan tag lebih dari 50% dengan game target. Untuk NDCG, relevansi dihitung berdasarkan tingkat kesamaan, dan skor dihitung menggunakan logaritma posisi setiap game dalam daftar rekomendasi.

### **Collaborative Filtering**

Pada sistem berbasis kolaborasi, evaluasi dilakukan dengan menggunakan **Mean Average Precision (MAP)** pada berbagai ambang batas *positive ratio* (60, 70, 80, dan 90). Hasil evaluasi menunjukkan bahwa baik rekomendasi berbasis pengguna maupun item berhasil mencapai MAP sebesar **1.000** untuk semua ambang batas. Ini berarti semua rekomendasi yang diberikan relevan dengan ambang batas tertentu, sehingga kinerja sistem dapat dianggap sangat baik.

Perhitungan MAP dilakukan dengan menghitung *precision* kumulatif untuk setiap item relevan yang ditemukan dalam daftar rekomendasi, kemudian dirata-ratakan. Hasil ini menunjukkan kemampuan model untuk memberikan rekomendasi yang sangat relevan, terutama dalam memenuhi preferensi pengguna pada rating positif yang tinggi.

### **Hybrid System**

Sistem hybrid menggabungkan beberapa informasi, seperti tag, deskripsi, dan platform, untuk memberikan rekomendasi yang lebih personal. Evaluasi dilakukan menggunakan **Mean Absolute Error (MAE)** pada data pengujian, yang menghasilkan nilai **0.1345**. Nilai MAE yang kecil ini menunjukkan bahwa prediksi rating oleh sistem sangat dekat dengan nilai aktualnya.

Selain itu, evaluasi pada data pelatihan memberikan metrik tambahan, yaitu **Mean Squared Error (MSE)** sebesar **0.058**, **Mean Absolute Error (MAE)** sebesar **0.186**, dan **Root Mean Squared Error (RMSE)** sebesar **0.242**. Metrik-metrik ini menunjukkan bahwa sistem hybrid memiliki performa yang sangat baik dalam memprediksi nilai relevansi game berdasarkan data yang digunakan.

Perhitungan metrik-metrik ini dilakukan dengan membandingkan prediksi model terhadap data aktual, kemudian menghitung rata-rata error menggunakan formula MSE, MAE, dan RMSE.

## Kesimpulan

1. EDA pada dataset rekomendasi membantu memahami pola, membersihkan data, dan mengevaluasi fitur yang relevan seperti genre, rating, dan platform.
2. Dalam pengembangan sistem rekomendasi game, pendekatan Content-based Filtering menggunakan fitur seperti tags, deskripsi, dan data historis pengguna memungkinkan rekomendasi yang lebih personal.
3. Hybrid Filtering menjadi solusi optimal dengan mengintegrasikan Content-based dan Collaborative Filtering untuk mengatasi keterbatasan seperti cold-start problem.
4. Efektivitas sistem rekomendasi diukur menggunakan metrik seperti Precision, Recall, MAE, dan RMSE, yang memastikan hasil akurat dan sesuai kebutuhan pengguna.
5. Sistem rekomendasi yang mempertimbangkan fitur seperti tags, deskripsi, platform, dan rating memberikan rekomendasi yang relevan dan kompatibel dengan preferensi serta perangkat pengguna.

## Referensi

1. Mulachela, A., Rizki, K., & Wahyuddin, Y. A. (2020). Analisis Perkembangan Industri Game di Indonesia Melalui Pendekatan Rantai Nilai Global (Global Value Chain). *Indonesian Journal of Global Discourse*, 2(2), 32-51. Retrieved from [Link](https://jtiik.ub.ac.id/index.php/jtiik/article/view/8503).

2. Syamkalla, M. T., Khomsah, S., & Nur, Y. S. R. (2024). Implementasi Algoritma Catboost Dan Shapley Additive Explanations (SHAP) Dalam Memprediksi Popularitas Game Indie Pada Platform Steam. *Jurnal Teknologi Informasi dan Ilmu Komputer, 11* (4), 777-786. Retrieved from [Link](https://ejournal.bsi.ac.id/ejurnal/index.php/ti/article/view/11462).

3. Ricci, F., Rokach, L., & Shapira, B. (2011). Introduction to Recommender Systems Handbook. In *Recommender Systems Handbook* (pp. 1-35). Springer. Retrieved from [Link](https://link.springer.com/chapter/10.1007/978-0-387-85820-3_1).

4. Resnick, P., Iacovou, N., Suchak, M., Bergstrom, P., & Riedl, J. (1994). GroupLens: An Open Architecture for Collaborative Filtering of Netnews. In *Proceedings of the 1994 ACM Conference on Computer Supported Cooperative Work* (pp. 175-186). ACM. Retrieved from [Link](https://dl.acm.org/doi/10.1145/192844.192905).

5. Burke, R. (2002). Hybrid Recommender Systems: Survey and Experiments. *User Modeling and User-Adapted Interaction, 12* (4), 331-370. Retrieved from [Link](https://link.springer.com/article/10.1023/A:1021240730564).

<!-- markdownlint-disable MD033 -->
</div>
<!-- markdownlint-enable MD033 -->
