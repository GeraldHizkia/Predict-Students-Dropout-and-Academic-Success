## KLASIFIKASI DROPOUT DAN KEBERHASILAN AKADEMIK MAHASISWA DENGAN SKENARIO PREDIKSI DINI DAN PENANGANAN DATA TIDAK SEIMBANG

## Dosen Pengampu :

## Ni Kadek Dwi Rusjayanthi, S.T., M.T.

## Mata Kuliah :

Data Mining E

## Disusun Oleh:

## Kendra Aurellia Renata – 2405551118 Tania Gracia Siwalette – 2405551116 Gerald Hizkia Turnip – 2405551081 Kezia Ardela Pinem – 2405551113

## PROGRAM STUDI TEKNOLOGI INFORMASI UNIVERSITAS UDAYANA FAKULTAS TEKNIK 2026


## PENDAHULUAN BAB I

## 1.1 Latar Belakang

Pendidikan tinggi merupakan salah satu aspek penting dalam meningkatkan kualitas

sumber daya manusia. Keberhasilan pendidikan tidak hanya dilihat dari jumlah mahasiswa

yang diterima, tetapi juga dari kemampuan mahasiswa dalam menyelesaikan pendidikannya.

Namun, dalam proses perkuliahan, terdapat mahasiswa yang mengalami berbagai kendala, baik

dari segi akademik maupun ekonomi, sehingga berpotensi berhenti melanjutkan pendidikan

atau mengalami dropout. Permasalahan ini perlu mendapatkan perhatian karena dapat

berdampak pada mahasiswa maupun institusi pendidikan.

Salah satu upaya yang dapat dilakukan untuk mengenali potensi permasalahan

tersebut adalah dengan memanfaatkan teknologi data mining. Data mining merupakan proses

pengolahan data untuk menemukan pola dan informasi yang bermanfaat. Dalam bidang

pendidikan, data mining dapat digunakan untuk menganalisis performa akademik serta

memprediksi status akhir mahasiswa. Salah satu metode yang dapat diterapkan adalah

klasifikasi, yaitu teknik untuk mengelompokkan data ke dalam kategori tertentu berdasarkan

pola dari data sebelumnya.

Penelitian ini menggunakan dataset Predict Students' Dropout and Academic Success

yang diperoleh dari UCI Machine Learning Repository. Dataset tersebut terdiri dari 4.424 data

mahasiswa dengan 36 atribut yang mencakup informasi demografi, jalur pendaftaran, latar

belakang keluarga, kondisi sosial ekonomi, serta data akademik semester pertama dan kedua.

Target klasifikasi dalam penelitian ini terdiri dari tiga kategori, yaitu Dropout, Enrolled, dan

Graduate.

Untuk memperoleh hasil klasifikasi yang optimal, penelitian ini membandingkan

beberapa algoritma, yaitu Decision Tree, Logistic Regression, K-Nearest Neighbors (KNN),

Random Forest, dan XGBoost. Selain itu, penelitian juga memperhatikan ketidakseimbangan

jumlah data pada setiap kelas dengan menguji pendekatan class weight dan Synthetic Minority

Over-sampling Technique (SMOTE). Pengujian dilakukan melalui tiga skenario prediksi, yaitu

menggunakan data saat pendaftaran, penambahan data akademik semester pertama, serta

penambahan data akademik semester pertama dan kedua.

Berdasarkan hal tersebut, penelitian ini dilakukan dengan judul "Klasifikasi Dropout

dan Keberhasilan Akademik Mahasiswa dengan Skenario Prediksi Dini dan Penanganan Data

Tidak Seimbang: Perbandingan Random Forest, XGBoost, dan Model Pembanding."

Penelitian ini bertujuan untuk mengetahui kinerja algoritma klasifikasi, menganalisis pengaruh


penambahan informasi akademik dan penanganan data tidak seimbang, serta mengidentifikasi

faktor-faktor yang berpengaruh terhadap status akhir mahasiswa. Hasil penelitian diharapkan

dapat memberikan gambaran mengenai pemanfaatan data mining sebagai pendekatan untuk

mendukung identifikasi dini mahasiswa yang berpotensi mengalami dropout.

## 1.2 Rumusan Masalah

Berdasarkan latar belakang yang telah diuraikan, rumusan masalah dalam penelitian

ini adalah sebagai berikut:

- 1. Algoritma klasifikasi manakah yang memiliki kinerja terbaik dalam memprediksi status akhir mahasiswa ke dalam kategori Dropout, Enrolled, dan Graduate?

- 2. Seberapa besar pengaruh penambahan data akademik semester pertama dan kedua terhadap peningkatan performa prediksi dibandingkan dengan penggunaan data saat pendaftaran mahasiswa saja?

- 3. Bagaimana pengaruh penerapan teknik penanganan data tidak seimbang, yaitu class weight dan SMOTE, terhadap kemampuan model dalam mengklasifikasikan setiap kelas, khususnya mahasiswa dengan status Dropout?

- 4. Faktor atau atribut apa saja yang memiliki pengaruh paling besar terhadap hasil klasifikasi status akhir mahasiswa?

## 1.3 Tujuan

Berdasarkan rumusan masalah tersebut, tujuan penelitian ini adalah:

- 1. Membangun dan membandingkan beberapa model klasifikasi untuk memprediksi status akhir mahasiswa menggunakan algoritma Decision Tree, Logistic Regression, KNN, Random Forest, dan XGBoost.

- 2. Mengetahui pengaruh penambahan informasi akademik semester pertama dan kedua terhadap performa model dalam melakukan prediksi status akhir mahasiswa.

- 3. Menganalisis pengaruh teknik penanganan data tidak seimbang, yaitu class weight dan SMOTE, terhadap performa klasifikasi, terutama dalam mendeteksi mahasiswa dengan status Dropout.

- 4. Mengidentifikasi atribut yang paling berpengaruh terhadap hasil klasifikasi status akhir mahasiswa melalui analisis Feature Importance, Permutation Importance, dan SHAP.

- 5. Menentukan model klasifikasi dengan kinerja terbaik berdasarkan hasil evaluasi menggunakan metrik yang telah ditentukan.


## 1.4 Manfaat

Penelitian ini diharapkan dapat memberikan manfaat baik secara akademik maupun

praktis sebagai berikut:

## 1.4.1 Manfaat Akademik

- 1. Menambah pemahaman mengenai penerapan data mining, khususnya metode klasifikasi dalam menganalisis dan memprediksi status akhir mahasiswa.

- 2. Memberikan pengalaman dalam menerapkan dan membandingkan berbagai algoritma klasifikasi, seperti Decision Tree, Logistic Regression, KNN, Random Forest, dan XGBoost.

- 3. Menambah pengetahuan mengenai penanganan ketidakseimbangan data menggunakan pendekatan class weight dan SMOTE.

- 4. Menjadi referensi bagi penelitian selanjutnya yang membahas prediksi dropout mahasiswa dan penerapan machine learning di bidang pendidikan.

## 1.4.2 Manfaat Praktis

- 1. Bagi Perguruan Tinggi: Memberikan gambaran mengenai pemanfaatan data mining untuk menganalisis status akademik mahasiswa dan mendukung identifikasi dini mahasiswa yang berpotensi mengalami dropout.

- 2. Bagi Mahasiswa: Memberikan pemahaman mengenai faktor-faktor yang berkaitan dengan keberhasilan akademik serta pentingnya memperhatikan perkembangan studi.

- 3. Bagi Peneliti: Menjadi sarana untuk menerapkan pengetahuan dan keterampilan dalam pengolahan data, pemodelan klasifikasi, evaluasi algoritma, serta interpretasi hasil machine learning.

- 4. Bagi Penelitian Selanjutnya: Menjadi bahan acuan untuk mengembangkan penelitian serupa


## LANDASAN TEORI BAB II

2.

- 2.1 Data Mining

Data mining merupakan proses pengolahan dan analisis data untuk menemukan pola,

hubungan, serta informasi yang memiliki nilai dan dapat digunakan dalam mendukung

pengambilan keputusan. Proses ini melibatkan penggunaan berbagai teknik komputasi dan

statistik untuk mengolah kumpulan data sehingga informasi yang sebelumnya sulit dikenali

dapat diperoleh.

Data mining dapat diterapkan dalam berbagai bidang, salah satunya adalah

pendidikan. Dalam bidang pendidikan, data mining dapat dimanfaatkan untuk menganalisis

data mahasiswa, mengidentifikasi pola perkembangan akademik, serta mengetahui faktor-

faktor yang berkaitan dengan keberhasilan studi. Hasil analisis tersebut dapat memberikan

informasi yang berguna bagi institusi pendidikan dalam memahami kondisi akademik

mahasiswa.

Salah satu penerapan data mining dalam penelitian ini adalah untuk menganalisis

status akhir mahasiswa berdasarkan sejumlah atribut yang tersedia dalam dataset. Melalui

proses pengolahan data dan penerapan algoritma klasifikasi, penelitian ini berupaya

menemukan pola yang dapat digunakan untuk memprediksi status mahasiswa ke dalam

kategori Dropout, Enrolled, dan Graduate.

- 2.2 Klasifikasi

Klasifikasi merupakan salah satu teknik dalam data mining yang digunakan untuk

mengelompokkan data ke dalam kategori atau kelas tertentu berdasarkan karakteristik yang

dimiliki. Teknik ini bekerja dengan mempelajari pola dari data yang telah memiliki label atau

kelas, kemudian menggunakan pola tersebut untuk menentukan kategori pada data yang belum

diketahui kelasnya.

Dalam proses klasifikasi, data umumnya dibagi menjadi data pelatihan (training data)

dan data pengujian (testing data). Data pelatihan digunakan untuk membangun model

berdasarkan pola yang tersedia, sedangkan data pengujian digunakan untuk mengetahui

kemampuan model dalam mengklasifikasikan data yang belum pernah digunakan selama

proses pelatihan.

Klasifikasi dapat digunakan untuk menyelesaikan permasalahan yang memiliki dua

kelas maupun lebih dari dua kelas. Pada penelitian ini, klasifikasi termasuk dalam kategori


multiclass classification karena model akan memprediksi status akhir mahasiswa ke dalam tiga

kelas, yaitu Dropout, Enrolled, dan Graduate. Setiap kelas memiliki karakteristik yang berbeda

sehingga model perlu mampu mengenali pola dari masing-masing kategori.

Penerapan klasifikasi dalam penelitian ini dilakukan dengan membandingkan

beberapa algoritma untuk mengetahui perbedaan kemampuan masing-masing metode dalam

memprediksi status akhir mahasiswa. Hasil klasifikasi nantinya akan dievaluasi menggunakan

sejumlah metrik untuk mengetahui tingkat ketepatan dan kemampuan model dalam mengenali

setiap kelas.

## 2.3 Algoritma Klasifikasi

Algoritma klasifikasi merupakan metode dalam machine learning yang digunakan

untuk mengelompokkan data ke dalam kategori tertentu berdasarkan pola yang dipelajari dari

data pelatihan. Dalam penelitian ini, algoritma klasifikasi digunakan untuk memprediksi status

akhir mahasiswa ke dalam tiga kategori, yaitu Dropout, Enrolled, dan Graduate.

Untuk memperoleh hasil klasifikasi yang optimal, penelitian ini menggunakan

beberapa algoritma sebagai pembanding, yaitu Decision Tree, Logistic Regression, K-Nearest

Neighbors (KNN), Random Forest, XGBoost, dan Majority Class Baseline. Adapun

perbandingan algoritma yang digunakan dapat dilihat pada Tabel beirkut.

| No. | Algoritma | Prinsip Kerja | Kelebihan | Kekurangan |
| --- | --- | --- | --- | --- |
| 1 |   | Decision Tree Membagi data berdasarkan atribut tertentu hingga membentuk struktur pohon keputusan. | Mudah dipahami, dapat menangani pola nonlinier, dan mudah diinterpretasikan. | Rentan mengalami overfitting jika pohon terlalu kompleks. |
| 2 | Logistic Regression | Menghitung probabilitas suatu data masuk ke kelas tertentu hubungan antarvariabel. | Sederhana, proses pelatihan relatif cepat, dan berdasarkan menghasilkan probabilitas. | Kurang optimal dalam menangkap pola nonlinier yang kompleks. |
|   | 3 K-Nearest Neighbors (KNN) | Menentukan kelas berdasarkan kemiripan dengan sejumlah tetangga terdekat. | Sederhana dan dapat digunakan untuk klasifikasi multikelas. | Sensitif terhadap skala data dan pemilihan nilai K. |
| 4 | Random Forest | Menggabungkan beberapa pohon keputusan dan menentukan hasil melalui majority voting. | Lebih stabil, mampu menangani banyak atribut, dan mengurangi risiko overfitting. | Membutuhkan komputasi lebih besar dan interpretasinya lebih kompleks. |


| 5 | XGBoost | Membangun pohon keputusan secara bertahap untuk memperbaiki kesalahan prediksi sebelumnya. | Mampu mempelajari pola kompleks dan mendukung regularisasi. | Memiliki banyak parameter yang perlu disesuaikan. |
| --- | --- | --- | --- | --- |
| 6 | Majority Class Baseline | Selalu memprediksi kelas dengan jumlah data terbanyak pada data pelatihan. | Sederhana dan menjadi standar pembanding awal. | Tidak mempelajari pola karakteristik setiap kelas. |

Berdasarkan perbandingan tersebut, Random Forest dan XGBoost menjadi algoritma

utama yang digunakan dalam penelitian ini. Sementara itu, Decision Tree, Logistic Regression,

dan KNN digunakan sebagai model pembanding. Majority Class Baseline digunakan untuk

mengetahui apakah model yang dibangun mampu memberikan hasil klasifikasi yang lebih baik

dibandingkan pendekatan prediksi sederhana.

## 2.4 Ketidakseimbangan Data (Imbalanced Data)

Ketidakseimbangan data (imbalanced data) merupakan kondisi ketika jumlah data

pada setiap kelas dalam suatu dataset memiliki perbedaan yang cukup besar. Kondisi ini dapat

menyebabkan model klasifikasi lebih cenderung mempelajari kelas mayoritas dibandingkan

kelas minoritas karena jumlah sampel kelas mayoritas lebih banyak.

Dalam proses klasifikasi, ketidakseimbangan data dapat memengaruhi kemampuan

model dalam mengenali setiap kategori. Model mungkin menghasilkan nilai akurasi yang

tinggi, tetapi kurang mampu memprediksi kelas yang memiliki jumlah data lebih sedikit. Oleh

karena itu, diperlukan teknik penanganan data tidak seimbang agar model dapat mempelajari

karakteristik setiap kelas dengan lebih baik.

Pada penelitian ini, penanganan ketidakseimbangan data dilakukan dengan

membandingkan pendekatan Class Weight dan Synthetic Minority Over-sampling Technique

(SMOTE), serta kondisi tanpa penanganan khusus sebagai pembanding.

## 2.4.1 Class Weight

Class Weight merupakan teknik penanganan ketidakseimbangan data dengan

memberikan bobot yang berbeda pada setiap kelas selama proses pelatihan model. Kelas yang

memiliki jumlah data lebih sedikit diberikan bobot lebih besar agar kesalahan prediksi pada

kelas tersebut mendapatkan perhatian lebih dalam proses pembelajaran.

Pemberian bobot bertujuan agar model tidak hanya berfokus pada kelas mayoritas,

tetapi juga memperhatikan kelas minoritas. Teknik ini tidak mengubah jumlah data dalam

dataset, melainkan menyesuaikan kontribusi setiap kelas terhadap proses pelatihan.


Secara umum, perhitungan bobot kelas dapat menggunakan rumus:

Keterangan:

- dV = Bobot kelas ke-i.

- 𝑁 = Jumlah seluruh data.

- \> = Jumlah kelas.

- [V = Jumlah data pada kelas ke-i.

Semakin sedikit jumlah data pada suatu kelas, semakin besar bobot yang dapat

diberikan kepada kelas tersebut.

Dalam penelitian ini, Class Weight diterapkan untuk mengetahui apakah pemberian

bobot pada kelas yang jumlah datanya lebih sedikit dapat meningkatkan kemampuan model

dalam mengklasifikasikan status akhir mahasiswa, khususnya kelas Dropout.

## 2.4.2 Synthetic Minority Over-sampling Technique (SMOTE)

Synthetic Minority Over-sampling Technique (SMOTE) merupakan metode yang

diperkenalkan oleh Chawla et al. (2002) untuk mengatasi ketidakseimbangan data dengan

menghasilkan sampel sintetis baru pada kelas minoritas.

Berbeda dengan teknik oversampling sederhana yang hanya menggandakan data yang

sudah tersedia, SMOTE membentuk data baru berdasarkan karakteristik sampel kelas

minoritas dan tetangga terdekatnya (nearest neighbors). Proses kerja SMOTE secara umum

meliputi:

- 1. Mengidentifikasi kelas minoritas dalam dataset.

- 2. Menentukan sejumlah tetangga terdekat dari setiap sampel kelas minoritas.

- 3. Memilih salah satu tetangga terdekat sebagai pasangan pembentukan sampel baru.

- 4. Menghasilkan sampel sintetis melalui interpolasi antara sampel awal dan tetangganya.

- 5. Mengulangi proses hingga jumlah sampel kelas minoritas mencapai jumlah yang ditentukan.

Rumus pembentukan sampel sintetis pada SMOTE adalah:

Keterangan:


- K[Rd = Sampel sintetis yang dihasilkan.

- KV = Sampel awal dari kelas minoritas.

- K[RVTO\_ = Sampel tetangga terdekat.

- ‐ = Nilai acak antara 0 dan 1.

Melalui proses tersebut, SMOTE dapat meningkatkan jumlah sampel pada kelas

minoritas sehingga distribusi data pelatihan menjadi lebih seimbang.

Dalam penelitian ini, SMOTE digunakan untuk mengetahui pengaruh penambahan

sampel sintetis terhadap performa algoritma klasifikasi dalam memprediksi status akhir

mahasiswa. Penerapannya dilakukan hanya pada data pelatihan, bukan data pengujian, untuk

menghindari kebocoran data (data leakage).

## 2.5 Evaluasi Model Klasifikasi

Evaluasi model klasifikasi dilakukan untuk mengukur kemampuan algoritma dalam

memprediksi status akhir mahasiswa. Penelitian ini menggunakan beberapa metrik evaluasi

yang disajikan pada Tabel berikut.

|   | No. Metrik Evaluasi | Penjelasan | Rumus |
| --- | --- | --- | --- |
| 1 | Confusion Matrix | Tabel yang digunakan untuk membandingkan hasil prediksi model dengan kelas sebenarnya, sehingga dapat diketahui jumlah prediksi benar dan salah pada setiap kelas. | Tidak memiliki rumus tunggal. Menggunakan TP, TN, FP, dan FN. |
| 2 | Accuracy | Mengukur persentase keseluruhan data yang berhasil diprediksi dengan benar oleh model. | 𝐴𝑐𝑐𝑢𝑟𝑎𝑐𝑦 Jumlah Prediksi Benar |
|   |   |   | = Total Data Pengujian |
| 3 | Precision | Mengukur ketepatan model dalam memprediksi suatu kelas dibandingkan dengan seluruh prediksi | 𝑃𝑟𝑒𝑐𝑖𝑠𝑖𝑜𝑛 = 𝑇𝑃 |
|   |   | pada kelas tersebut. | 𝑇𝑃 + 𝐹𝑃 |
| 4 | Recall | Mengukur kemampuan model dalam menemukan seluruh data yang sebenarnya termasuk ke dalam | 𝑅𝑒𝑐𝑎𝑙𝑙 = 𝑇𝑃 |
|   |   | suatu kelas. | 𝑇𝑃 + 𝐹𝑁 |
| 5 | Macro-F1 Score | Menghitung rata-rata F1-Score seluruh kelas dengan memberikan bobot yang sama pada setiap kelas. | 𝐾 1 𝑀𝑎𝑐𝑟𝑜-𝐹1 = ∑𝐹 1𝑖 𝐾 𝑖=1 |


|   | 6 Weighted- F1 Score | Menghitung rata-rata F1-Score seluruh kelas dengan mempertimbangkan jumlah data pada masing- masing kelas. | 𝐾 𝑛𝑖 𝑊𝑒𝑖𝑔ℎ𝑡𝑒𝑑-𝐹1 =∑ × 𝐹1𝑖 𝑁 𝑖=1 |
| --- | --- | --- | --- |

Berdasarkan metrik tersebut, penelitian ini menggunakan Macro-F1 Score sebagai

metrik evaluasi utama karena memberikan bobot yang sama terhadap kelas Dropout, Enrolled,

dan Graduate, sehingga sesuai untuk mengevaluasi dataset dengan distribusi kelas yang tidak

seimbang. Sementara itu, metrik lainnya digunakan sebagai evaluasi pendukung.

## 2.6 Cross-Validation dan Hyperparameter Tuning

Cross-Validation merupakan teknik validasi yang digunakan untuk mengevaluasi

kemampuan model machine learning dengan membagi data pelatihan menjadi beberapa bagian

(fold). Teknik ini bertujuan untuk mengetahui kestabilan performa model serta mengurangi

ketergantungan hasil evaluasi terhadap satu pembagian data tertentu.

Salah satu teknik yang digunakan adalah K-Fold Cross-Validation, yaitu membagi

data menjadi sejumlah bagian dengan ukuran yang relatif sama. Pada setiap iterasi, satu bagian

digunakan sebagai data validasi, sedangkan bagian lainnya digunakan untuk melatih model.

Proses tersebut dilakukan secara bergantian hingga seluruh bagian pernah digunakan sebagai

data validasi.

Dalam penelitian ini digunakan Stratified 5-Fold Cross-Validation, yaitu teknik

validasi yang membagi data pelatihan menjadi lima bagian dengan tetap mempertahankan

proporsi kelas Dropout, Enrolled, dan Graduate pada setiap fold. Teknik ini sesuai digunakan

karena dataset penelitian memiliki distribusi kelas yang tidak seimbang.

Selain Cross-Validation, penelitian ini juga menerapkan Hyperparameter Tuning,

yaitu proses pencarian kombinasi parameter terbaik yang mengatur proses pembelajaran

algoritma agar menghasilkan performa klasifikasi yang optimal. Setiap algoritma memiliki

hyperparameter yang berbeda dan dapat memengaruhi hasil prediksi.

Metode pencarian parameter yang digunakan adalah RandomizedSearchCV, yaitu

teknik pencarian hyperparameter dengan mencoba sejumlah kombinasi parameter yang dipilih

secara acak dari ruang pencarian yang telah ditentukan. Setiap kombinasi dievaluasi

menggunakan Cross-Validation untuk memperoleh konfigurasi model terbaik berdasarkan

metrik evaluasi yang ditetapkan.


Melalui penerapan Cross-Validation dan Hyperparameter Tuning, diharapkan model

klasifikasi dapat menghasilkan performa yang lebih stabil dan optimal dalam memprediksi

status akhir mahasiswa, yaitu Dropout, Enrolled, dan Graduate.

## 2.7 Interpretasi Model

Interpretasi model merupakan proses untuk memahami faktor-faktor yang

memengaruhi hasil prediksi algoritma machine learning. Dalam penelitian ini, interpretasi

dilakukan menggunakan Feature Importance, Permutation Importance, dan SHAP untuk

mengetahui atribut yang berkontribusi terhadap klasifikasi status akhir mahasiswa.

| No. | Metode | Penjelasan | Tujuan Penggunaan |
| --- | --- | --- | --- |
| 1 |   | Feature Importance Metode untuk mengukur tingkat kepentingan setiap atribut berdasarkan kontribusinya dalam proses pembentukan prediksi model. | Mengetahui atribut yang dianggap paling penting oleh model dalam memprediksi status akhir mahasiswa. |
| 2 | Permutation Importance | Metode yang mengukur kepentingan atribut dengan cara mengacak nilai suatu fitur dan melihat perubahan performa model. | Mengetahui seberapa besar pengaruh suatu atribut terhadap performa klasifikasi. |
| 3 | SHAP (SHapley Additive exPlanations) | Metode interpretasi yang menghitung kontribusi setiap atribut terhadap hasil prediksi model, termasuk arah dan besarnya pengaruh. | Menjelaskan bagaimana suatu atribut berkontribusi terhadap prediksi kelas Dropout, Enrolled, dan Graduate. |

Berdasarkan ketiga metode tersebut, penelitian ini diharapkan dapat mengidentifikasi

atribut yang paling berpengaruh terhadap hasil klasifikasi. Hasil interpretasi juga digunakan

untuk memahami pola karakteristik mahasiswa yang berkaitan dengan status akhir

akademiknya.

## 2.8 Gambaran Umum Objek Penelitian

Objek penelitian ini adalah permasalahan klasifikasi status akhir mahasiswa

berdasarkan informasi demografi, latar belakang keluarga, kondisi sosial ekonomi, serta

perkembangan akademik. Permasalahan ini berfokus pada pengelompokan mahasiswa ke

dalam kategori Dropout, Enrolled, dan Graduate berdasarkan karakteristik yang terdapat pada

data mahasiswa.


Penelitian ini menggunakan pendekatan data mining dengan metode klasifikasi untuk

mengidentifikasi pola yang berkaitan dengan status akhir mahasiswa. Pengujian direncanakan

menggunakan beberapa algoritma klasifikasi untuk membandingkan kemampuan masing-

masing metode dalam memprediksi kategori status mahasiswa. Selain itu, penelitian juga

memperhatikan ketidakseimbangan jumlah data pada setiap kategori agar kemampuan model

dalam mengenali kelas minoritas tetap dapat dievaluasi.

Objek penelitian ini tidak menggunakan data mahasiswa dari perguruan tinggi di

Indonesia, melainkan menggunakan dataset terbuka yang berasal dari salah satu institusi

pendidikan di Portugal. Oleh karena itu, penelitian ini berfokus pada pengujian metode

klasifikasi menggunakan dataset acuan (benchmark) dan tidak dimaksudkan untuk

menggambarkan secara langsung kondisi mahasiswa pada peambaran Umum Objek Penelitian.

## 2.9 Alur Penelitian (CRISP-DM)

Penelitian ini menggunakan kerangka kerja CRISP-DM (Cross-Industry Standard

Process for Data Mining) sebagai pedoman dalam melaksanakan tahapan penelitian secara

sistematis. Kerangka kerja ini digunakan untuk mengatur proses penelitian mulai dari

memahami karakteristik data, melakukan persiapan data, membangun model klasifikasi,

hingga mengevaluasi dan menginterpretasikan hasil prediksi.

Dalam penelitian ini, tahapan CRISP-DM disesuaikan dengan kebutuhan penelitian

mengenai klasifikasi dropout dan keberhasilan akademik mahasiswa. Adapun tahapan

penelitian yang dilakukan adalah sebagai berikut.


Gambar di atas merupakan alur penelitian yang menggambarkan tahapan pelaksanaan

penelitian menggunakan metode CRISP-DM (Cross-Industry Standard Process for Data

Mining. Adapun penjelasan dari setiap tahapan tersebut adalah sebagai berikut:

- Pemahaman Data (Data Understanding), Tahap ini dilakukan untuk memahami dataset yang digunakan melalui pemeriksaan karakteristik data, distribusi kelas, serta identifikasi atribut yang tersedia.

- Persiapan Data (Data Preparation), tahap ini meliputi proses pembersihan data, encoding atribut kategorikal, standardisasi, pembentukan fitur baru (feature engineering), dan pembagian data menjadi data pelatihan serta pengujian.

- Pemodelan (Modeling), tahap ini dilakukan dengan menerapkan algoritma Decision Tree, Logistic Regression, K-Nearest Neighbors (KNN), Random Forest, dan XGBoost, serta Majority Class Baseline sebagai model pembanding.

- Penanganan Data Tidak Seimbang dan Penyetelan Hyperparameter, tahap ini dilakukan dengan membandingkan teknik Class Weight dan SMOTE untuk menangani ketidakseimbangan data, serta melakukan hyperparameter tuning menggunakan Stratified 5-Fold Cross-Validation.

- Evaluasi pada Data Uji (Evaluation), tahap ini bertujuan mengukur performa model menggunakan Accuracy, Precision, Recall, Macro-F1 Score, Weighted-F1 Score, dan Confusion Matrix untuk menentukan model dengan hasil klasifikasi terbaik.

- Interpretasi dan Rekomendasi, tahap terakhir dilakukan dengan menganalisis hasil prediksi menggunakan Feature Importance, Permutation Importance, dan SHAP. Hasil analisis digunakan untuk mengetahui atribut yang berpengaruh terhadap status akhir mahasiswa serta menyusun rekomendasi penelitian.

## 2.10 Gambaran Umum Dataset

Dataset yang digunakan dalam penelitian ini adalah Predict Students' Dropout and

Academic Success yang diperoleh dari UCI Machine Learning Repository dengan ID 697.

Dataset ini dikembangkan oleh Realinho, Vieira Martins, Machado, dan Baptista pada tahun

2021 dari Instituto Politécnico de Portalegre, Portugal. Dataset tersebut dapat diakses secara

terbuka melalui situs UCI Machine Learning Repository dengan DOI 10.24432/C5MC89 dan

menggunakan lisensi Creative Commons Attribution 4.0 (CC BY 4.0).

Dataset ini terdiri dari 4.424 baris data mahasiswa dengan 36 atribut prediktor dan

satu atribut target. Setiap baris merepresentasikan satu mahasiswa, sedangkan atribut yang


tersedia mencakup informasi demografi, jalur pendaftaran, latar belakang keluarga, kondisi

sosial ekonomi, perkembangan akademik, dan kondisi makroekonomi. Data tersedia dalam

format CSV dan dapat digunakan untuk keperluan analisis maupun pemodelan klasifikasi.

## 2.10.1 Sumber dan Karakteristik Dataset

Dataset Predict Students' Dropout and Academic Success diperoleh melalui UCI

Machine Learning Repository dan berasal dari data mahasiswa Instituto Politécnico de

Portalegre. Data tersebut mencakup beberapa program studi, seperti Agronomi, Desain,

Pendidikan, Keperawatan, Jurnalistik, Manajemen, Pekerjaan Sosial, dan Teknologi. Secara

umum, dataset memiliki karakteristik sebagai berikut:

| Aspek | Keterangan |
| --- | --- |
| Nama Dataset | Predict Students' Dropout and Academic Success |
| Sumber | UCI Machine Learning Repository |
| ID Dataset | 697 |
| Pembuat | Realinho, Vieira Martins, Machado, Baptista (2021) |
| Institusi | Instituto Politécnico de Portalegre, Portugal |
| DOI | 10.24432/C5MC89 |
| Lisensi | CC BY 4.0 |
| Format | CSV |
| Jumlah Data | 4.424 baris |
| Jumlah Atribut | 36 fitur dan 1 target |
| Tipe Data | Integer, real, dan kategorikal |
| Nilai Hilang | Tidak terdapat nilai hilang berdasarkan dokumentasi UCI |

## 2.10.2 Variabel Target

Variabel target merupakan atribut yang menjadi tujuan utama dalam proses klasifikasi.

Pada dataset Predict Students' Dropout and Academic Success, variabel target terdiri dari tiga

kategori yang menunjukkan status akhir mahasiswa.

| Kelas | Keterangan |
| --- | --- |
| Dropout | Mahasiswa yang berhenti atau tidak melanjutkan pendidikan |
| Enrolled | Mahasiswa yang masih terdaftar atau melanjutkan studi |
| Graduate | Mahasiswa yang telah menyelesaikan pendidikan dan dinyatakan lulus |


Ketiga kategori tersebut menjadi kelas yang akan diprediksi oleh model klasifikasi

dalam penelitian ini. Berdasarkan dokumentasi dataset, distribusi jumlah data pada setiap kelas

tidak seimbang, dengan kelas Graduate memiliki jumlah data paling banyak, diikuti Dropout,

kemudian Enrolled. Kondisi tersebut menjadi salah satu pertimbangan dalam pengujian teknik

penanganan data tidak seimbang.

## 2.10.3 Kelompok Atribut

Dataset memiliki 36 atribut prediktor yang dapat dikelompokkan berdasarkan

informasi yang direpresentasikan. Pengelompokan ini bertujuan untuk mempermudah

pemahaman terhadap karakteristik data serta melihat jenis informasi yang dapat digunakan

dalam proses klasifikasi.

| Kelompok Atribut | Contoh Atribut | Keterangan |
| --- | --- | --- |
| Demografi | Marital status, Gender, Age at enrollment, Nationality, International | Menggambarkan karakteristik pribadi mahasiswa |
| Jalur Pendaftaran | Application mode, Application order, Course, Daytime/evening attendance, Previous qualification, Admission grade | Berisi informasi terkait proses pendaftaran dan penerimaan mahasiswa |
| Latar Belakang Keluarga | Mother's qualification, Father's qualification, Mother's occupation, Father's occupation | Menggambarkan latar belakang pendidikan dan pekerjaan orang tua |
| Sosial Ekonomi | Scholarship holder, Debtor, Tuition fees up to date, Displaced, Educational special needs | Menggambarkan kondisi sosial dan ekonomi mahasiswa |
| Akademik Semester Pertama | Curricular units 1st sem: credited, enrolled, evaluations, approved, grade, without evaluations | Menggambarkan perkembangan akademik mahasiswa pada semester pertama |
| Akademik Semester Kedua | Curricular units 2nd sem: credited, enrolled, evaluations, approved, grade, without evaluations | Menggambarkan perkembangan akademik mahasiswa pada semester kedua |
| Makroekonomi | Unemployment rate, Inflation rate, GDP | Menggambarkan kondisi ekonomi pada periode pengumpulan data |

Atribut-atribut tersebut memiliki karakteristik dan jenis informasi yang berbeda.

Beberapa atribut berbentuk kategorikal tetapi direpresentasikan menggunakan angka, sehingga

perlu diperhatikan dalam proses pengolahan data agar nilai numerik tidak langsung dianggap

memiliki tingkatan atau urutan tertentu.


## 2.10.4 Karakteristik dan Keterbatasan Dataset

Dataset yang digunakan memiliki beberapa karakteristik yang perlu diperhatikan

sebelum diterapkan dalam proses klasifikasi. Salah satunya adalah ketidakseimbangan jumlah

sampel pada ketiga kelas target, sehingga model berpotensi lebih mudah mengenali kelas

dengan jumlah data dominan dibandingkan kelas lainnya. Selain itu, dokumentasi UCI

menyatakan bahwa dataset tidak memiliki nilai hilang, tetapi kondisi tersebut tetap perlu

diperiksa kembali ketika proses eksplorasi data dilakukan.

Karakteristik lainnya adalah penggunaan data dari institusi pendidikan di Portugal,

sehingga hasil pengujian tidak dapat langsung dianggap mewakili kondisi pendidikan tinggi di

Indonesia. Beberapa atribut kategorikal juga dikodekan dalam bentuk angka, seperti Course

dan Application mode, sehingga diperlukan penanganan yang sesuai ketika proses

preprocessing dilakukan. Dengan mempertimbangkan karakteristik tersebut, dataset ini

digunakan sebagai dataset acuan untuk menguji dan membandingkan metode klasifikasi dalam

memprediksi status akhir mahasiswa.
