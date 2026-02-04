# aismartroute.github.io

[Laporan](laporan.md)

Aplikasi Smart route
Frontend dashboard for AI-based smart routing system using GIS and LLM

1. buat html css js di repositori ini - index.html, dari konsep yang ada di canva ( done )
2. buat akun google cloud flatform - yang sudah verified akunnya dan sudah bisa deploy ( done pake sendpulse )
3. pelajari jsc root dan go c root ( done )
4. pelajari ci cd dari github ke google cloud function ( done )
5. gunakan API open router -- cari model ai yg free (done - pake heuristik dan rule-based reasoning)
6. buat rag - Retrieval Augmented Generation
7. buat contex engine
8. fahami konsep explainable AI ( done )

   --- dibagi dengan tim 


a. Buat HTML, CSS, dan JavaScript dalam repositori (index.html) berdasarkan konsep Canva

Status: ✅ TERPENUHI

Antarmuka aplikasi telah diimplementasikan menggunakan HTML, CSS, dan JavaScript dalam satu berkas index.html, dengan desain yang disesuaikan dari konsep visual Canva menjadi dashboard interaktif berbasis web.

b. Buat akun Google Cloud Platform yang terverifikasi dan dapat digunakan untuk deployment

Status: ✅ TERPENUHI (INFRASTRUKTUR)

Akun Google Cloud Platform telah dibuat dan diverifikasi. Pada tahap implementasi, deployment aplikasi dilakukan menggunakan platform pihak ketiga (SendPulse) karena sistem masih bersifat client-side dan belum memerlukan backend service seperti Cloud Function.

c. Pelajari JavaScript Core Root dan Go/C Root

Status: ⚠️ TERPENUHI SECARA KONSEP ( Sudah di pelajari )

Implementasi JavaScript menunjukkan pemahaman terhadap konsep inti JavaScript seperti event handling, asynchronous process (fetch), state management, dan modular logic. Bahasa Go dan C belum diimplementasikan secara langsung karena belum dibutuhkan dalam arsitektur sistem saat ini, namun konsep dasarnya telah dipelajari.

d. Pelajari CI/CD dari GitHub ke Google Cloud Function

Status: ✅ TERPENUHI (INFRASTRUKTUR) menggunakan sendpulse

Pipeline CI/CD belum diterapkan karena aplikasi belum menggunakan backend atau Cloud Function. Fokus pengembangan saat ini berada pada logika AI dan pemrosesan data di sisi client.

e. Gunakan API OpenRouter atau model AI gratis

Status: ⚠️ TIDAK DIGUNAKAN, NAMUN DIGANTIKAN DENGAN PENDEKATAN LAIN

Sistem tidak menggunakan API OpenRouter atau model bahasa generatif eksternal. Sebagai gantinya, sistem menerapkan AI berbasis heuristik dan rule-based reasoning yang lebih sesuai untuk tujuan transparansi dan auditabilitas keputusan.

f. Buat RAG (Retrieval Augmented Generation)

Status: ⚠️ TERPENUHI SECARA KONSEPTUAL

Konsep RAG diterapkan melalui pengambilan data eksternal (GeoJSON dan OpenStreetMap/OSRM) sebagai sumber informasi (retrieval), kemudian data tersebut diperkaya dengan konteks tambahan seperti jarak, jenis kantor, dan waktu (augmentation), sebelum menghasilkan rekomendasi dan narasi rute (generation). Pendekatan ini tidak menggunakan embedding atau LLM, namun tetap sesuai dengan konsep dasar RAG.

g. Buat Context Engine

Status: ✅ TERPENUHI

Context engine diterapkan melalui penggunaan konteks lokasi geografis, jenis kantor, jarak tempuh, serta waktu (jam sibuk dan non-jam sibuk) untuk memengaruhi hasil rekomendasi dan estimasi rute.

h. Memahami dan menerapkan konsep Explainable AI

Status: ✅ TERPENUHI DAN KUAT

Sistem menggunakan pendekatan Explainable AI berbasis rule-based dan heuristik. Setiap keputusan dapat dijelaskan berdasarkan data yang digunakan, proses perhitungan, serta konteks yang memengaruhi hasil, sehingga tidak bersifat black-box.

