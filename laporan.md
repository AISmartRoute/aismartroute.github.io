<div align="center">

# TUGAS BESAR  
## Mata Kuliah Artificial Intelligence

# PENGEMBANGAN SISTEM SMART ROUTING BERBASIS ARTIFICIAL INTELLIGENCE  
## PADA DASHBOARD POS SMARTROUTING  
### MENGGUNAKAN PENDEKATAN BERBASIS LEKSIKON PADA KOMENTAR YOUTUBE

---

### Oleh :

**RISKA RAFIELA MUSLIMAH – 714252005**  

**RIZQI AKDAM KURNIA – 714252015**  

**FAJAR KURNIA ROHMAN – 714252028**  

**ASEP MULYADI – 714252023**  

**ADY CHANDRA – 714252010**


<img width="567" height="207" alt="image" src="https://github.com/user-attachments/assets/945fea9b-29e1-4ccb-a237-e8fc87678b1e" />


### Program Studi Sarjana Terapan Teknik Informatika  
**UNIVERSITAS LOGISTIK DAN BISNIS INTERNASIONAL**  
**2026**

</div>

---

## DAFTAR ISI

- [BAB I PENDAHULUAN](#bab-i-pendahuluan)
  - [1.1 Latar Belakang](#11-latar-belakang)
  - [1.2 Tujuan Proyek](#12-tujuan-proyek)
  - [1.3 Ruang Lingkup Proyek](#13-ruang-lingkup-proyek)
  - [1.4 Sistematika Penulisan Laporan](#14-sistematika-penulisan-laporan)

- [BAB II DESKRIPSI SISTEM](#bab-ii-deskripsi-sistem)
  - [2.1 Gambaran Umum Sistem](#21-gambaran-umum-sistem)
  - [2.2 Tujuan Fungsional Sistem](#22-tujuan-fungsional-sistem)
  - [2.3 Fitur Utama Sistem](#23-fitur-utama-sistem)
    - [2.3.1 Peta Interaktif](#231-peta-interaktif)
    - [2.3.2 Visualisasi Rute Jalan Nyata](#232-visualisasi-rute-jalan-nyata)
    - [2.3.3 Manajemen Data Lokasi](#233-manajemen-data-lokasi)
    - [2.3.4 AI Route Assistant](#234-ai-route-assistant)
    - [2.3.5 Estimasi Waktu Bebasis Konteks](#235-estimasi-waktu-bebasis-konteks)
  - [2.4 Alur Kerja Sistem](#24-alur-kerja-sistem)
  - [2.5 Karakteristik Sistem](#25-karakteristik-sistem)

- [BAB III ARSITEKTUR & TEKNOLOGI](#bab-iii-arsitektur--teknologi)
  - [3.1 Arsitektur Sistem](#31-arsitektur-sistem)
  - [3.2 Komponen Arsitektur Sistem](#32-komponen-arsitektur-sistem)
    - [3.2.1 Lapisan Antar Muka ( User Interface Layer )](#321-lapisan-antar-muka--user-interface-layer-)
    - [3.2.2 Lapisan Logika ( Application Logic Layer )](#322-lapisan-logika--application-logic-layer-)
    - [3.2.3 Lapisan Data dan GIS](#323-lapisan-data-dan-gis)
  - [3.3 Arsitektur Alur Sistem](#33-arsitektur-alur-sistem)
  - [3.4 Teknologi yang Digunakan](#34-teknologi-yang-digunakan)
  - [3.5 Alasan Pemilihan Teknologi](#35-alasan-pemilihan-teknologi)
  - [3.6 Keterkaitan Arsitektur denagn Konsep AI](#36-keterkaitan-arsitektur-denagn-konsep-ai)

- [BAB IV SUMBER DAN KARAKTERISTIK DATA](#bab-iv-sumber-dan-karakteristik-data)
  - [4.1 Gambaran Umum Data](#41-gambaran-umum-data)
  - [4.2 Jenis Data yang Digunakan](#42-jenis-data-yang-digunakan)
    - [4.2.1 Data Utama](#421-data-utama)
    - [4.2.2 Data Pendukung](#422-data-pendukung)
  - [4.3 Sumber Data](#43-sumber-data)
  - [4.4 Karakteristik Data](#44-karakteristik-data)
  - [4.5 Proses Pengolahan Data dalam Sistem](#45-proses-pengolahan-data-dalam-sistem)
  - [4.6 Peran Data dalam Sistem AI](#46-peran-data-dalam-sistem-ai)
  - [4.7 Keterbatasan Data](#47-keterbatasan-data)

- [BAB V IMPLEMENTASI DAN PENJELASAN KODE](#bab-v-implementasi-dan-penjelasan-kode)
  - [5.1 Gambaran Umum Implementasi](#51-gambaran-umum-implementasi)
  - [5.2 Struktur Umum Kode](#52-struktur-umum-kode)
  - [5.3 Manajemen Konfigurasi dan State Aplikasi](#53-manajemen-konfigurasi-dan-state-aplikasi)
  - [5.4 Inisialisasi dan Visualisasi Peta](#54-inisialisasi-dan-visualisasi-peta)
  - [5.5 Pemrosesan Data GeoJSON ( Data Statis )](#55-pemrosesan-data-geojson--data-statis-)
  - [5.6 Penempatan Marker dan Daftar Lokasi](#56-penempatan-marker-dan-daftar-lokasi)
  - [5.7 Implementasi Routing Jalan Nyata](#57-implementasi-routing-jalan-nyata)
  - [5.8 Pemrosesan Input Pengguna ( AI Route Assistant )](#58-pemrosesan-input-pengguna--ai-route-assistant-)
  - [5.9 Implementasi Context Engine](#59-implementasi-context-engine)
  - [5.10 Implementasi Heuristic Scoring](#510-implementasi-heuristic-scoring)
  - [5.11 Pembuatan Narasi Route ( Explainable Output )](#511-pembuatan-narasi-route--explainable-output-)
  - [5.12 Penegasan Implementasi AI dengan Data Statis](#512-penegasan-implementasi-ai-dengan-data-statis)

- [BAB VI IMPLEMENTASI ARTIFICIAL INTELLIGENCE](#bab-vi-implementasi-artificial-intelligence)
  - [6.1 Konsep Artificial Intelligence yang Diterapkan](#61-konsep-artificial-intelligence-yang-diterapkan)
  - [6.2 Arsitektur Logika AI](#62-arsitektur-logika-ai)
  - [6.3 Rule Based Reasoning](#63-rule-based-reasoning)
  - [6.4 Heuristic Decision Making](#64-heuristic-decision-making)
  - [6.5 Context Engine](#65-context-engine)
  - [6.6 Implementasi Explainable AI](#66-implementasi-explainable-ai)
  - [6.7 Keterkaitan AI dengan Data Statis](#67-keterkaitan-ai-dengan-data-statis)
  - [6.8 Evaluasi Implementasi AI](#68-evaluasi-implementasi-ai)

- [BAB VII EVALUASI REQUIREMENT PROYEK](#bab-vii-evaluasi-requirement-proyek)
  - [7.1 Evaluasi Requirement Teknis dan Konseptual](#71-evaluasi-requirement-teknis-dan-konseptual)
    - [7.1.1 Pengembangan HTML, CSS, dan JavaScript](#711-pengembangan-html-css-dan-javascript)
    - [7.1.2 Pembuatan Akun Google Cloud Platform dan Deployment](#712-pembuatan-akun-google-cloud-platform-dan-deployment)
    - [7.1.3 Pemahaman JavaScript Core Root dan Go/C Root](#713-pemahaman-javascript-core-root-dan-goc-root)
    - [7.1.4 Penerapan CI/CD dari GitHub ke Google Cloud Function](#714-penerapan-cicd-dari-github-ke-google-cloud-function)
    - [7.1.5 Penggunaan API OpenRouter dan Model AI Gratis](#715-penggunaan-api-openrouter-dan-model-ai-gratis)
    - [7.1.6 Implementasi Retrieval Augmented Generation ( RAG )](#716-implementasi-retrieval-augmented-generation--rag-)
    - [7.1.7 Implementasi Contex Engine](#717-implementasi-contex-engine)
    - [7.1.8 Penerapan Explainable AI](#718-penerapan-explainable-ai)
  - [7.2 Ringkasan Evaluasi](#72-ringkasan-evaluasi)

- [BAB VIII KESIMPULAN DAN SARAN](#bab-viii-kesimpulan-dan-saran)
  - [8.1 Kesimpulan](#81-kesimpulan)
  - [8.2 Saran Pengembangan](#82-saran-pengembangan)
  - [8.3 Penutup](#83-penutup)


---

# BAB I PENDAHULUAN

## Latar Belakang

Dalam sistem logistik dan distribusi, perencanaan rute pengiriman merupakan aspek krusial yang berpengaruh langsung terhadap efisiensi waktu, biaya operasional, serta kualitas layanan. Penentuan rute yang kurang optimal dapat menyebabkan keterlambatan pengiriman, pemborosan sumber daya, dan penurunan kepuasan pengguna. Oleh karena itu, diperlukan suatu sistem yang mampu membantu pengambilan keputusan rute secara cepat, akurat, dan terstruktur.

Perkembangan teknologi Artificial Intelligence (AI) dan Geographic Information System (GIS) memungkinkan pemrosesan data geografis dilakukan secara sistematis untuk mendukung perencanaan rute. AI tidak selalu harus diwujudkan dalam bentuk model pembelajaran mesin atau model bahasa generatif, tetapi juga dapat diterapkan melalui pendekatan rule-based reasoning, heuristic decision making, dan context-aware system, terutama pada sistem yang membutuhkan transparansi dan keterjelasan proses pengambilan keputusan.

Berdasarkan kebutuhan tersebut, dikembangkan proyek POS SmartRouting AI Dashboard, yaitu sebuah aplikasi frontend berbasis web yang berfungsi sebagai dashboard interaktif untuk visualisasi peta, penentuan rute jalan nyata, serta rekomendasi rute pengiriman. Sistem ini memanfaatkan data geografis statis yang diperoleh dari luar program, dikombinasikan dengan layanan peta dan routing publik, serta logika AI berbasis heuristik yang dapat dijelaskan (Explainable AI).

Pendekatan ini dipilih untuk menekankan aspek pemahaman konsep AI, keterjelasan alur logika, serta kemudahan evaluasi akademik, tanpa ketergantungan pada backend service atau model AI generatif eksternal.

## 1.2 Tujuan Proyek

Tujuan dari pengembangan proyek POS SmartRouting AI Dashboard adalah sebagai berikut:

- Mengembangkan sebuah dashboard frontend berbasis web untuk sistem smart routing pengiriman.
- Mengintegrasikan peta digital dan data geografis (GIS) untuk visualisasi lokasi dan rute.
- Menerapkan pendekatan Artificial Intelligence berbasis heuristik dan rule-based reasoning.
- Mengimplementasikan sistem berbasis konteks (context-aware system) dalam estimasi rute dan waktu tempuh.
- Menerapkan prinsip Explainable AI, sehingga setiap keputusan sistem dapat ditelusuri dan dijelaskan.
- Menyediakan fondasi sistem yang siap dikembangkan lebih lanjut ke arsitektur backend atau AI generatif di masa depan.

## 1.3 Ruang Lingkup Proyek

Ruang lingkup proyek ini dibatasi pada aspek-aspek berikut:

- Pengembangan aplikasi frontend-only menggunakan HTML, CSS, dan JavaScript.
- Penggunaan data lokasi kantor pos dalam format GeoJSON yang bersifat statis dan diperoleh dari luar program.
- Integrasi layanan peta OpenStreetMap dan routing OSRM untuk penentuan jalur jalan nyata.
- Implementasi logika AI berbasis heuristik, rule-based reasoning, dan context engine.
- Penyajian hasil dalam bentuk visualisasi peta, rekomendasi rute, estimasi waktu, dan narasi rute.

Adapun aspek yang tidak termasuk dalam ruang lingkup proyek ini meliputi:

- Pengembangan backend service atau API
- Penggunaan database terpusat
- Implementasi machine learning berbasis pelatihan data
- Penggunaan model bahasa generatif (LLM) secara langsung

---

# BAB II DESKRIPSI SISTEM

## 2.1 Gambaran Umum Sistem

POS SmartRouting AI Dashboard merupakan aplikasi berbasis web yang dirancang sebagai sistem pendukung keputusan (Decision Support System) untuk membantu proses perencanaan dan visualisasi rute pengiriman. Sistem ini berfokus pada pemanfaatan data geografis dan logika Artificial Intelligence (AI) berbasis heuristik untuk menghasilkan rekomendasi rute yang kontekstual dan dapat dijelaskan.

Aplikasi dikembangkan sebagai frontend-only system, di mana seluruh proses pengolahan data, perhitungan rute, serta logika AI dijalankan di sisi klien (client-side). Pendekatan ini memungkinkan sistem diakses langsung melalui peramban web tanpa memerlukan instalasi perangkat lunak tambahan atau koneksi ke backend service.

Sistem memanfaatkan data lokasi kantor pos yang bersifat statis dan telah disiapkan sebelumnya dalam format GeoJSON. Data tersebut dipadukan dengan layanan peta dan routing publik untuk menampilkan jalur jalan nyata serta menghasilkan estimasi waktu tempuh dan narasi rute berbasis konteks.

## 2.2 Tujuan Fungsional Sistem

Secara fungsional, sistem ini dirancang untuk:

* Menyediakan visualisasi peta interaktif lokasi kantor pos.
* Menampilkan rute jalan nyata antar lokasi berdasarkan input pengguna.
* Memberikan estimasi jarak dan waktu tempuh rute pengiriman.
* Menghasilkan rekomendasi kantor terdekat atau rute optimal berdasarkan logika AI.
* Menyajikan penjelasan rute dalam bentuk narasi yang mudah dipahami pengguna.

## 2.3 Fitur Utama Sistem

Fitur-fitur utama yang diimplementasikan dalam sistem meliputi:

### 2.3.1 Peta Interaktif

Sistem menyediakan peta digital interaktif yang menampilkan:

* Lokasi kantor pos dalam bentuk marker
* Informasi lokasi yang ditampilkan melalui popup
* Navigasi peta seperti zoom dan pan

Peta dibangun menggunakan library GIS berbasis JavaScript yang memungkinkan interaksi langsung dengan pengguna.

### 2.3.2 Visualisasi Rute Jalan Nyata

Sistem mampu menampilkan rute jalan nyata antara dua lokasi kantor pos. Rute dihitung menggunakan layanan routing publik dan divisualisasikan langsung pada peta, sehingga pengguna dapat melihat jalur pengiriman yang direkomendasikan secara visual.

### 2.3.3 Manajemen Data Lokasi

Sistem menampilkan daftar kantor pos yang bersumber dari data GeoJSON statis. Informasi yang disajikan meliputi:

* Nama kantor
* Alamat
* Jenis kantor
* Lokasi geografis

Data ini menjadi dasar bagi seluruh proses perhitungan rute dan rekomendasi AI.

### 2.3.4 AI Route Assistant

Sistem dilengkapi dengan modul AI Route Assistant berbasis antarmuka chat. Pengguna dapat memasukkan perintah berbasis teks, seperti permintaan rute antar kantor atau rekomendasi kantor terdekat.

Modul ini berfungsi sebagai penghubung antara input pengguna dan logika AI yang ada di dalam sistem.

### 2.3.5 Estimasi Waktu Bebasis Konteks

Estimasi waktu tempuh rute tidak hanya bergantung pada jarak, tetapi juga mempertimbangkan konteks waktu, khususnya kondisi jam sibuk dan non-jam sibuk. Penyesuaian waktu dilakukan menggunakan aturan heuristik yang telah ditentukan.

## 2.4 Alur Kerja Sistem

Secara umum, alur kerja sistem dapat dijelaskan sebagai berikut:

1. Sistem memuat data lokasi kantor pos dari berkas GeoJSON statis.
2. Data lokasi divisualisasikan pada peta sebagai marker.
3. Pengguna memasukkan perintah atau permintaan rute melalui antarmuka chat.
4. Sistem memproses input pengguna dan mencocokkannya dengan data lokasi.
5. Layanan routing publik digunakan untuk menghitung rute jalan nyata.
6. Context engine mengevaluasi kondisi waktu dan konteks lainnya.
7. Sistem menghasilkan rekomendasi rute, estimasi waktu, dan narasi penjelasan.
8. Hasil ditampilkan pada peta dan pada modul AI Route Assistant.

## 2.5 Karakteristik Sistem

Karakteristik utama dari sistem ini adalah:

**Client-Side Processing**

Seluruh logika dijalankan di sisi klien tanpa backend service.

**Data Statis**

Data lokasi bersifat statis dan diperoleh dari luar program.

**Explainable AI**

Keputusan sistem dapat dijelaskan secara logis dan transparan.

**Modular dan Extensible**

Sistem dirancang agar mudah dikembangkan lebih lanjut, misalnya dengan penambahan backend atau integrasi AI generatif.

---

# BAB III ARSITEKTUR & TEKNOLOGI

## 3.1 Arsitektur Sistem

POS SmartRouting AI Dashboard dirancang menggunakan arsitektur client-side application, di mana seluruh proses pengolahan data, visualisasi peta, serta logika Artificial Intelligence (AI) dijalankan di sisi klien (client). Sistem tidak bergantung pada backend service atau server aplikasi, sehingga dapat diakses langsung melalui peramban web.

Pemilihan arsitektur ini didasarkan pada tujuan proyek yang menitikberatkan pada pemahaman konsep AI, keterjelasan alur logika, serta kemudahan evaluasi akademik. Selain itu, arsitektur client-side memungkinkan sistem dikembangkan dan dideploy secara sederhana menggunakan platform statis.

## 3.2 Komponen Arsitektur Sistem

Secara umum, arsitektur sistem terdiri dari tiga komponen utama, yaitu:

### 3.2.1 Lapisan Antar Muka ( User Interface Layer )

Lapisan antarmuka bertanggung jawab dalam menampilkan informasi kepada pengguna dan menerima input pengguna. Komponen ini diimplementasikan menggunakan:

* HTML untuk struktur halaman
* CSS dan Tailwind CSS untuk pengaturan tampilan dan layout

Antarmuka dirancang sebagai dashboard interaktif yang memadukan peta, daftar data, dan modul AI Route Assistant.

### 3.2.2 Lapisan Logika ( Application Logic Layer )

Lapisan logika diimplementasikan menggunakan JavaScript dan berfungsi sebagai inti pemrosesan sistem. Tanggung jawab lapisan ini meliputi:

* Pengelolaan state aplikasi
* Pemrosesan data GeoJSON
* Pengendalian peta dan marker
* Pemanggilan layanan routing
* Implementasi logika AI berbasis heuristik
* Pengelolaan context engine dan explainability

Seluruh logika AI dan pengambilan keputusan berada pada lapisan ini.

### 3.2.3 Lapisan Data dan GIS

Lapisan data menyediakan informasi yang dibutuhkan oleh sistem, meliputi:

* Data lokasi kantor pos dalam format GeoJSON (data statis)
* Data peta digital dari OpenStreetMap
* Data rute jalan dari layanan OSRM

Lapisan ini bersifat read-only dan tidak dimodifikasi oleh sistem selama proses berjalan.

## 3.3 Arsitektur Alur Sistem

Alur arsitektur sistem dapat dirangkum sebagai berikut:

1. Data GeoJSON dimuat ke dalam memori aplikasi.
2. Data divisualisasikan dalam bentuk marker pada peta.
3. Input pengguna diproses oleh modul logika.
4. Layanan routing publik digunakan untuk menghitung rute jalan.
5. Context engine mengevaluasi kondisi tambahan.
6. Logika AI menghasilkan rekomendasi dan narasi.
7. Hasil ditampilkan pada antarmuka pengguna.

Arsitektur ini memastikan pemisahan yang jelas antara data, logika, dan tampilan.

## 3.4 Teknologi yang Digunakan

Teknologi yang digunakan dalam pengembangan sistem ditunjukkan pada Tabel 3.1.

**Tabel 3.1 Teknologi yang Digunakan**

| Komponen           | Teknologi                          |
| ------------------ | ---------------------------------- |
| Bahasa Pemrograman | JavaScript                         |
| Markup & Styling   | HTML, CSS, Tailwind CSS            |
| GIS Library        | Leaflet.js                         |
| Routing Engine     | OSRM (Open Source Routing Machine) |
| Data Format        | GeoJSON                            |
| Deployment         | GitHub Pages / SendPulse           |
| Pendekatan AI      | Heuristic & Rule-Based Reasoning   |

## 3.5 Alasan Pemilihan Teknologi

Pemilihan teknologi didasarkan pada pertimbangan sebagai berikut:

**HTML, CSS, dan JavaScript**

Dipilih karena bersifat standar, ringan, dan mudah di-deploy sebagai aplikasi frontend.

**Leaflet.js**

Digunakan karena bersifat open-source, ringan, dan mendukung visualisasi GIS interaktif.

**OpenStreetMap dan OSRM**

Menyediakan data peta dan rute jalan nyata secara terbuka dan dapat diakses tanpa biaya.

**GeoJSON**

Merupakan format standar untuk data geografis yang mudah diproses di sisi klien.

**Pendekatan AI Heuristik**

Dipilih untuk memastikan sistem bersifat transparan, mudah dijelaskan, dan sesuai dengan konsep Explainable AI.

## 3.6 Keterkaitan Arsitektur denagn Konsep AI

Arsitektur sistem mendukung penerapan AI berbasis reasoning melalui:

* Pemisahan logika AI dari data statis
* Penggunaan context engine sebagai pengambil keputusan
* Kemampuan penelusuran setiap keputusan ke data dan aturan yang digunakan

Dengan demikian, arsitektur yang dirancang tidak hanya mendukung fungsi teknis, tetapi juga memperkuat aspek konseptual Artificial Intelligence yang dapat dijelaskan.

---

# BAB IV SUMBER DAN KARAKTERISTIK DATA

## 4.1 Gambaran Umum Data

Data merupakan komponen utama dalam pengembangan sistem POS SmartRouting AI Dashboard. Seluruh proses visualisasi peta, penentuan rute, serta pengambilan keputusan AI dalam sistem ini bergantung pada data geografis yang telah disiapkan sebelumnya. Data yang digunakan bersifat statis dan diperoleh dari luar program utama, sehingga sistem tidak melakukan proses pengumpulan data secara real time.

Pendekatan ini dipilih untuk memfokuskan pengembangan pada aspek logika Artificial Intelligence, pemrosesan konteks, dan explainability, tanpa ketergantungan pada sistem backend atau sumber data dinamis.

## 4.2 Jenis Data yang Digunakan

Data yang digunakan dalam sistem dapat diklasifikasikan menjadi dua jenis utama, yaitu data utama dan data pendukung.

### 4.2.1 Data Utama

Data utama berupa informasi lokasi kantor pos yang disimpan dalam format GeoJSON. Data ini mencakup:

* Nama kantor pos
* Jenis kantor (misalnya KCU, KCP)
* Alamat lengkap
* Informasi wilayah administratif
* Koordinat geografis (latitude dan longitude)

Data ini digunakan sebagai basis utama untuk seluruh proses pemetaan, pencarian lokasi, dan rekomendasi rute.

### 4.2.2 Data Pendukung

Selain data utama, sistem memanfaatkan data pendukung berupa:

* Data peta digital dari OpenStreetMap
* Data rute jalan dari Open Source Routing Machine (OSRM)

Data pendukung ini diakses melalui layanan publik dan digunakan secara read-only, tanpa penyimpanan permanen di dalam sistem.

## 4.3 Sumber Data

Sumber data dalam proyek ini meliputi:

**Berkas GeoJSON statis**

Data lokasi kantor pos yang telah dikumpulkan dan diproses di luar program utama, kemudian disimpan sebagai berkas GeoJSON.

**Layanan Peta Publik**

OpenStreetMap digunakan sebagai sumber data peta dasar.

**Layanan Routing Publik**

OSRM digunakan untuk menghitung rute jalan nyata antar lokasi.

Seluruh sumber data yang digunakan bersifat terbuka dan tidak memerlukan autentikasi atau biaya penggunaan.

## 4.4 Karakteristik Data

Karakteristik data yang digunakan dalam sistem adalah sebagai berikut:

**Statis**

Data lokasi tidak berubah selama sistem berjalan dan tidak diperbarui secara otomatis.

**Terstruktur**

Data disimpan dalam format GeoJSON yang memiliki struktur standar dan konsisten.

**Spasial**

Data mengandung informasi geografis yang dapat dipetakan dan dihitung jaraknya.

**Read-Only**

Sistem hanya membaca data tanpa melakukan modifikasi atau penulisan ulang.

## 4.5 Proses Pengolahan Data dalam Sistem

Meskipun data bersifat statis, sistem tetap melakukan proses pengolahan data secara dinamis, meliputi:

* Pembacaan data GeoJSON secara asynchronous
* Normalisasi data ke dalam objek JavaScript
* Penyimpanan data ke dalam memori aplikasi
* Pemanfaatan data untuk visualisasi peta
* Penggunaan data sebagai input logika AI dan context engine

Dengan demikian, data statis berfungsi sebagai knowledge base yang diproses secara kontekstual oleh sistem.

## 4.6 Peran Data dalam Sistem AI

Dalam sistem POS SmartRouting AI Dashboard, data tidak hanya berfungsi sebagai informasi pasif, tetapi juga sebagai:

* Dasar pengambilan keputusan AI
* Input utama heuristic scoring
* Sumber konteks lokasi dan jarak
* Basis explainability hasil sistem

Keputusan AI selalu dapat ditelusuri kembali ke data yang digunakan dan aturan yang diterapkan.

## 4.7 Keterbatasan Data

Beberapa keterbatasan data dalam proyek ini antara lain:

* Tidak adanya data lalu lintas real time
* Data lokasi tidak diperbarui secara otomatis
* Ketergantungan pada akurasi data eksternal

Keterbatasan ini menjadi dasar pertimbangan untuk pengembangan sistem di masa men

---

# BAB V IMPLEMENTASI DAN PENJELASAN KODE

## 5.1 Gambaran Umum Implementasi

Implementasi sistem POS SmartRouting AI Dashboard dilakukan menggunakan pendekatan single-page frontend application yang seluruh komponennya ditempatkan dalam satu berkas index.html. Di dalam berkas tersebut, struktur antarmuka, gaya tampilan, dan logika pemrosesan sistem diintegrasikan secara terpadu.

Pendekatan ini dipilih untuk:

* Menyederhanakan proses deployment
* Memudahkan evaluasi kode secara menyeluruh
* Menghindari kompleksitas arsitektur backend pada tahap awal

Meskipun seluruh sistem berjalan di sisi klien, struktur kode tetap disusun secara modular melalui pemisahan fungsi dan tanggung jawab masing-masing bagian.

## 5.2 Struktur Umum Kode

Secara umum, struktur kode terbagi menjadi tiga bagian utama:

**Struktur HTML**

Digunakan untuk membangun elemen antarmuka seperti peta, daftar data, tab navigasi, dan modul AI Route Assistant.

**Styling CSS**

Digunakan untuk mengatur tampilan visual dashboard, termasuk layout, warna, tipografi, dan interaksi antarmuka.

**Logika JavaScript**

Digunakan untuk mengelola data, memproses input pengguna, menghitung rute, serta mengimplementasikan logika Artificial Intelligence.

## 5.3 Manajemen Konfigurasi dan State Aplikasi

Sistem menggunakan beberapa variabel global untuk menyimpan konfigurasi dan state aplikasi, antara lain:

* Konfigurasi awal dashboard
* Objek peta Leaflet
* Daftar marker lokasi
* Data kantor pos hasil pemrosesan GeoJSON
* Objek rute aktif pada peta

State ini memungkinkan sistem untuk:

* Mengelola perubahan tampilan peta
* Menghindari duplikasi marker
* Mengontrol satu rute aktif dalam satu waktu

## 5.4 Inisialisasi dan Visualisasi Peta

Peta diinisialisasi menggunakan library Leaflet dengan titik awal yang telah ditentukan. OpenStreetMap digunakan sebagai sumber peta dasar. Setelah peta siap, sistem menambahkan marker berdasarkan data lokasi yang telah dimuat.

Proses ini mencakup:

* Pembuatan objek peta
* Penambahan layer peta
* Penempatan marker berdasarkan koordinat geografis
* Penambahan popup informasi pada setiap marker

Visualisasi ini berfungsi sebagai dasar interaksi pengguna dengan sistem.

## 5.5 Pemrosesan Data GeoJSON ( Data Statis )

Data lokasi kantor pos dimuat menggunakan mekanisme asynchronous melalui fungsi fetch. Berkas GeoJSON diproses dan dinormalisasi menjadi objek JavaScript dengan struktur yang seragam.

Tahapan pemrosesan data meliputi:

* Pembacaan berkas GeoJSON
* Ekstraksi properti dan koordinat geografis
* Konversi data ke dalam format numerik
* Penyimpanan hasil pemrosesan ke dalam memori aplikasi

Data yang telah diproses tidak diubah oleh sistem dan berfungsi sebagai knowledge base statis.

## 5.6 Penempatan Marker dan Daftar Lokasi

Setelah data dimuat, sistem menampilkan:

* Marker lokasi pada peta
* Daftar kantor pos pada panel daftar

Setiap entitas lokasi ditampilkan secara konsisten baik pada peta maupun pada daftar, sehingga pengguna dapat memahami keterkaitan antara tampilan visual dan data tekstual.

## 5.7 Implementasi Routing Jalan Nyata

Perhitungan rute jalan nyata dilakukan menggunakan Leaflet Routing Machine yang terhubung dengan layanan OSRM publik. Sistem menentukan dua titik (asal dan tujuan) berdasarkan input pengguna, kemudian mengirimkan koordinat tersebut ke layanan routing.

Hasil perhitungan rute meliputi:

* Jalur jalan yang divisualisasikan pada peta
* Jarak tempuh
* Waktu tempuh dasar

Sistem tidak menghitung rute secara mandiri, melainkan memanfaatkan hasil routing sebagai input untuk proses AI selanjutnya.

## 5.8 Pemrosesan Input Pengguna ( AI Route Assistant )

Modul AI Route Assistant menerima input pengguna dalam bentuk teks. Sistem melakukan pemrosesan sederhana untuk:

* Mengidentifikasi pola perintah (misalnya permintaan rute)
* Menormalisasi teks input
* Mencocokkan input dengan data lokasi yang tersedia

Pendekatan ini memungkinkan interaksi berbasis bahasa natural tanpa menggunakan model bahasa generatif.

## 5.9 Implementasi Context Engine

Context engine berfungsi untuk menambahkan dimensi kontekstual dalam pengambilan keputusan. Salah satu konteks utama yang digunakan adalah waktu, khususnya pembagian antara jam sibuk dan non-jam sibuk.

Berdasarkan konteks waktu tersebut, sistem:

* Menyesuaikan estimasi waktu tempuh
* Menambahkan informasi kondisi lalu lintas pada narasi rute

Pendekatan ini membuat hasil sistem bersifat adaptif terhadap situasi tertentu.

## 5.10 Implementasi Heuristic Scoring

Sistem menerapkan heuristic scoring untuk menentukan rekomendasi lokasi atau rute. Skor dihitung berdasarkan beberapa faktor, antara lain:

* Jarak geografis antara pengguna dan lokasi
* Jenis kantor pos

Setiap faktor memiliki bobot yang telah ditentukan sebelumnya, sehingga proses perhitungan bersifat eksplisit dan dapat dijelaskan.

## 5.11 Pembuatan Narasi Route ( Explainable Output )

Salah satu fitur utama sistem adalah kemampuan menghasilkan narasi rute. Narasi ini disusun berdasarkan:

* Data rute hasil OSRM
* Nama jalan
* Jarak tempuh
* Konteks waktu

Narasi yang dihasilkan bersifat deskriptif dan mudah dipahami, serta dapat ditelusuri kembali ke data dan aturan yang digunakan.

## 5.12 Penegasan Implementasi AI dengan Data Statis

Meskipun sistem menggunakan data statis, implementasi AI tetap valid karena:

* Sistem melakukan reasoning berbasis aturan
* Keputusan dihasilkan melalui evaluasi konteks
* Output bersifat dinamis berdasarkan input pengguna

Dengan demikian, sistem tidak hanya menampilkan data, tetapi juga melakukan proses pengambilan keputusan berbasis Artificial Intelligence.

---

# BAB VI IMPLEMENTASI ARTIFICIAL INTELLIGENCE

## 6.1 Konsep Artificial Intelligence yang Diterapkan

Artificial Intelligence (AI) dalam proyek POS SmartRouting AI Dashboard diterapkan sebagai sistem pengambilan keputusan berbasis reasoning, bukan sebagai model pembelajaran mesin (machine learning) atau model bahasa generatif. Pendekatan ini menempatkan AI sebagai mekanisme logika yang mampu mengevaluasi data, konteks, dan aturan untuk menghasilkan rekomendasi yang adaptif dan dapat dijelaskan.

Pendekatan AI yang digunakan mencakup:

* Rule-Based Reasoning
* Heuristic Decision Making
* Context-Aware System

Pendekatan tersebut dipilih untuk memastikan transparansi keputusan, kemudahan audit, serta kesesuaian dengan prinsip Explainable AI.

## 6.2 Arsitektur Logika AI

Logika AI diimplementasikan pada lapisan aplikasi (application logic layer) dan terdiri dari beberapa komponen utama, yaitu:

* Modul pemrosesan input pengguna
* Modul pencarian dan pencocokan data lokasi
* Modul heuristic scoring
* Context engine
* Modul pembentukan output dan narasi

Setiap komponen memiliki peran yang jelas dan saling terintegrasi dalam menghasilkan keputusan akhir.

## 6.3 Rule Based Reasoning

Rule-based reasoning digunakan untuk menentukan alur keputusan sistem berdasarkan aturan eksplisit yang telah ditetapkan. Contoh aturan yang diterapkan antara lain:

* Jika input pengguna mengandung pola permintaan rute, maka sistem memproses permintaan routing.
* Jika input pengguna mengandung kata kunci tertentu (misalnya “terdekat”), maka sistem menjalankan logika rekomendasi lokasi.

Aturan ini memungkinkan sistem untuk merespons input pengguna secara konsisten dan dapat diprediksi.

## 6.4 Heuristic Decision Making

Heuristic decision making digunakan untuk memberikan skor dan peringkat pada alternatif keputusan. Dalam sistem ini, heuristik diterapkan pada proses rekomendasi lokasi dan rute.

Faktor-faktor yang digunakan dalam heuristic scoring meliputi:

* Jarak geografis
* Jenis kantor pos
* Bobot kepentingan masing-masing faktor

Skor akhir dihitung menggunakan kombinasi bobot yang telah ditentukan, sehingga setiap keputusan dapat dijelaskan secara matematis.

## 6.5 Context Engine

Context engine berfungsi untuk memperkaya proses pengambilan keputusan dengan informasi tambahan di luar data utama. Konteks utama yang digunakan dalam sistem ini adalah:

* Konteks waktu, yaitu pembagian antara jam sibuk dan non-jam sibuk
* Konteks lokasi, yaitu posisi relatif antara pengguna dan tujuan

Context engine memengaruhi:

* Estimasi waktu tempuh
* Narasi rute
* Informasi kondisi lalu lintas yang ditampilkan

Dengan demikian, keputusan sistem tidak bersifat statis, tetapi menyesuaikan dengan situasi tertentu.

## 6.6 Implementasi Explainable AI

Sistem dirancang dengan prinsip Explainable AI (XAI), di mana setiap keputusan yang dihasilkan dapat dijelaskan secara logis dan terstruktur. Explainability diwujudkan melalui:

* Aturan eksplisit

Seluruh keputusan didasarkan pada aturan dan heuristik yang jelas.

* Proses yang dapat ditelusuri

Setiap output dapat ditelusuri kembali ke data dan konteks yang digunakan.

* Narasi deskriptif

Sistem menghasilkan narasi rute yang menjelaskan jalur, jarak, dan kondisi secara natural.

Pendekatan ini memastikan sistem tidak bersifat black-box.

## 6.7 Keterkaitan AI dengan Data Statis

Meskipun data lokasi yang digunakan bersifat statis, implementasi AI tetap valid karena:

* Sistem melakukan reasoning terhadap data
* Keputusan dipengaruhi oleh konteks dan input pengguna
* Output bersifat dinamis dan adaptif

Dengan demikian, AI dalam sistem ini berfungsi sebagai decision logic, bukan sebagai sekadar visualisasi data.

## 6.8 Evaluasi Implementasi AI

Implementasi AI dalam sistem ini memiliki kelebihan sebagai berikut:

* Transparan dan mudah dijelaskan
* Tidak bergantung pada API AI eksternal
* Cocok untuk lingkungan yang membutuhkan akuntabilitas tinggi

Namun, sistem juga memiliki keterbatasan, antara lain:

* Tidak memanfaatkan pembelajaran dari data historis
* Tidak menggunakan data lalu lintas real time

Keterbatasan ini menjadi dasar pengembangan sistem di masa depan.

---

# BAB VII EVALUASI REQUIREMENT PROYEK

## 7.1 Evaluasi Requirement Teknis dan Konseptual

Bab ini membahas evaluasi ketercapaian requirement proyek POS SmartRouting AI Dashboard berdasarkan tujuan dan ketentuan awal pengembangan. Evaluasi dilakukan untuk menilai sejauh mana setiap requirement telah dipenuhi, baik secara implementatif maupun konseptual, serta untuk mengidentifikasi keterbatasan dan potensi pengembangan lanjutan.

Setiap requirement dievaluasi secara terpisah dengan penjelasan mengenai status pencapaiannya.

### 7.1.1 Pengembangan HTML, CSS, dan JavaScript

Antarmuka aplikasi telah diimplementasikan menggunakan HTML, CSS, dan JavaScript dalam satu berkas index.html. Desain dashboard disesuaikan dari konsep visual yang telah dibuat sebelumnya, kemudian diimplementasikan menjadi aplikasi web interaktif. Seluruh fitur utama sistem, termasuk peta, daftar lokasi, dan AI Route Assistant, berhasil dijalankan menggunakan teknologi frontend tersebut.

### 7.1.2 Pembuatan Akun Google Cloud Platform dan Deployment

Akun Google Cloud Platform telah dibuat dan diverifikasi. Namun, pada tahap implementasi saat ini, aplikasi dideploy menggunakan platform statis (GitHub Pages dan SendPulse) karena sistem belum memerlukan backend service atau Cloud Function. Secara konseptual, infrastruktur cloud telah dipersiapkan untuk pengembangan lanjutan.

### 7.1.3 Pemahaman JavaScript Core Root dan Go/C Root

Implementasi JavaScript dalam proyek ini menunjukkan pemahaman terhadap konsep inti JavaScript, seperti event handling, asynchronous processing, pengelolaan state, dan modularisasi logika. Bahasa Go dan C tidak diimplementasikan secara langsung dalam sistem karena belum dibutuhkan dalam arsitektur saat ini, namun konsep dasarnya telah dipelajari sebagai landasan pengembangan backend di masa depan.

### 7.1.4 Penerapan CI/CD dari GitHub ke Google Cloud Function

Konsep CI/CD telah dipelajari dan dipahami. Namun, pipeline CI/CD belum diimplementasikan secara aktif karena sistem belum menggunakan backend atau Cloud Function. Fokus pengembangan saat ini berada pada logika AI dan pemrosesan data di sisi client.

### 7.1.5 Penggunaan API OpenRouter dan Model AI Gratis

Sistem tidak menggunakan API OpenRouter atau model bahasa generatif eksternal. Sebagai gantinya, digunakan pendekatan AI berbasis heuristik dan rule-based reasoning. Pendekatan ini dipilih untuk menjamin transparansi, konsistensi, dan kemudahan audit keputusan sistem.

### 7.1.6 Implementasi Retrieval Augmented Generation ( RAG )

Konsep RAG diterapkan secara konseptual melalui:

* Pengambilan data eksternal (GeoJSON dan OSRM) sebagai proses retrieval
* Penambahan konteks jarak, jenis kantor, dan waktu sebagai augmentation
* Pembentukan rekomendasi dan narasi rute sebagai generation

Meskipun tidak menggunakan embedding atau LLM, pendekatan ini tetap sejalan dengan prinsip dasar RAG.

### 7.1.7 Implementasi Contex Engine

Context engine telah diimplementasikan melalui pemanfaatan konteks lokasi dan waktu. Konteks ini digunakan untuk memengaruhi estimasi waktu tempuh dan narasi rute, sehingga hasil sistem bersifat adaptif terhadap situasi tertentu.

### 7.1.8 Penerapan Explainable AI

Sistem menerapkan prinsip Explainable AI secara konsisten. Setiap keputusan dihasilkan melalui aturan dan heuristik yang eksplisit, serta disertai penjelasan dalam bentuk narasi rute. Sistem tidak bersifat black-box dan seluruh proses pengambilan keputusan dapat ditelusuri.

## 7.2 Ringkasan Evaluasi

Secara keseluruhan, sebagian besar requirement proyek telah terpenuhi, baik secara implementatif maupun konseptual. Beberapa requirement yang belum diterapkan secara penuh disebabkan oleh pertimbangan ruang lingkup proyek dan arsitektur sistem yang masih bersifat frontend-only.

Pendekatan ini tetap dinilai relevan dan sesuai dengan tujuan pembelajaran serta pengemb

---

# BAB VIII KESIMPULAN DAN SARAN

## 8.1 Kesimpulan

Berdasarkan hasil perancangan, implementasi, dan evaluasi yang telah dilakukan, dapat disimpulkan bahwa proyek POS SmartRouting AI Dashboard berhasil mengembangkan sebuah sistem smart routing berbasis Artificial Intelligence yang berfokus pada transparansi, konteks, dan keterjelasan proses pengambilan keputusan.

Sistem ini mengintegrasikan data geografis statis dalam format GeoJSON dengan layanan peta dan routing publik untuk menghasilkan visualisasi rute jalan nyata, estimasi waktu tempuh, serta rekomendasi rute pengiriman. Pendekatan Artificial Intelligence yang digunakan tidak bergantung pada model pembelajaran mesin atau model bahasa generatif, melainkan memanfaatkan rule-based reasoning, heuristic decision making, dan context-aware system.

Implementasi AI dalam sistem ini memenuhi prinsip Explainable AI, di mana setiap keputusan dapat dijelaskan secara logis berdasarkan data, aturan, dan konteks yang digunakan. Meskipun menggunakan data statis dan arsitektur frontend-only, sistem tetap mampu menghasilkan output yang dinamis dan adaptif terhadap input pengguna.

Dengan demikian, proyek ini menunjukkan bahwa sistem Artificial Intelligence yang efektif dan dapat dipertanggungjawabkan tidak selalu memerlukan kompleksitas model pembelajaran mesin, terutama dalam konteks sistem pendukung keputusan berbasis logika dan transparansi.

## 8.2 Saran Pengembangan

Berdasarkan keterbatasan dan hasil evaluasi proyek, beberapa saran pengembangan yang dapat dilakukan di masa mendatang antara lain:

* **Pengembangan Backend Service**
  Menambahkan backend service atau REST API untuk pengelolaan data dinamis dan integrasi sistem yang lebih kompleks.

* **Integrasi Database Spasial**
  Menggunakan database spasial untuk menyimpan dan memperbarui data lokasi secara terpusat.

* **Implementasi CI/CD Otomatis**
  Menerapkan pipeline CI/CD dari GitHub ke Google Cloud Function untuk mendukung pengembangan dan deployment berkelanjutan.

* **Integrasi Model AI Generatif**
  Mengintegrasikan model bahasa generatif melalui OpenRouter untuk meningkatkan kemampuan interaksi bahasa natural dan analisis rute.

* **Penerapan RAG Berbasis Embedding**
  Mengembangkan RAG dengan embedding untuk meningkatkan relevansi rekomendasi berbasis konteks historis dan pengetahuan tambahan.

* **Penggunaan Data Lalu Lintas Real Time**
  Mengintegrasikan data lalu lintas real time untuk meningkatkan akurasi estimasi waktu tempuh.

## 8.3 Penutup

Laporan proyek ini diharapkan dapat memberikan gambaran yang komprehensif mengenai penerapan Artificial Intelligence berbasis reasoning dalam sistem smart routing. Pendekatan yang digunakan dalam proyek ini dapat menjadi referensi bagi pengembangan sistem AI yang menekankan aspek explainability, akuntabilitas, dan keterjelasan proses pengambilan keputusan.

---





