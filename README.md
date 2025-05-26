<div align="Left">
  
## Squad Girls  
# Optimalisasi Alokasi Fiskal dalam Peningkatan Pembangunan Manusia Menuju Indonesia Emas 2045
## Deskripsi Proyek
Repositori ini merupakan bagian dari tugas akhir mata kuliah Statistika Machine Learning, yang bertujuan menganalisis efektivitas alokasi fiskal antarprovinsi dalam meningkatkan Indeks Pembangunan Manusia (IPM) dan mengentaskan kemiskinan (Desil 1), dalam kerangka visi Indonesia Emas 2045

## Latar Belakang
Visi Indonesia Emas 2045 menekankan pentingnya pertumbuhan inklusif dan berkelanjutan. Namun, tantangan fiskal nasional yang dihadapi adalah ketimpangan antarprovinsi dalam hal alokasi dan efektivitas penggunaan anggaran. Oleh karena itu, urgensi mengarahkan fiskal ke outcome nyata seperti peningkatan Indeks Pembangunan Manusia (IPM) dan pengentasan kemiskinan menjadi sangat penting. Fakta menunjukan bahwa Distribusi IPM antarprovinsi menunjukkan bahwa sebagian besar provinsi memiliki IPM antara 70–75, namun terdapat beberapa provinsi dengan IPM sangat rendah (<60) dan sangat tinggi (>80). Ini mengindikasikan adanya ketimpangan pembangunan manusia yang cukup tajam antarwilayah. Meskipun ada beberapa wilayah provinsi memiliki alokasi fiskal (PAGU APBN) cukup besar, tidak semua menunjukkan peningkatan signifikan pada IPM. Hal ini menandakan perlunya klasifikasi efektivitas penggunaan anggaran berbasis data sebagai dasar penyusunan kebijakan yang lebih tepat sasaran.

## Tujuan Penelitian
Proyek ini bertujuan untuk:
- Menganalisis hubungan antara alokasi fiskal provinsi, Indeks Pembangunan Manusia (IPM), dan distribusi kelompok miskin Desil 1 di seluruh Indonesia.
- Mengetahui efektivitas penggunaan anggaran, dengan asumsi bahwa jika pagu anggaran tinggi namun IPM tetap rendah, maka penggunaan anggaran tersebut belum optimal dalam
  meningkatkan kesejahteraan manusia.
- Mengklasifikasikan provinsi ke dalam kategori efektif atau tidak efektif dalam penggunaan fiskal, menggunakan pendekatan Tree-Based Classification (CART & Random Forest),
  yang akan dijadikan dasar rekomendasi kebijakan fiskal untuk mewujudkan visi Indonesia Emas 2045.

## Sumber Data 
1. Sumber data: Satu Data (data.go.id), 
2. Indeks Pembangunan Manusia 2024 (bps.go.id), 
3. Data Demografi Kesejahteraan Masyarakat-Desil 1 (data-go.id)

## Variabel
- PAGU APBN 2024 dan Provinsi (Alokasi fiskal) => Variabel Predictor
- IPM_2024 (Outcome pembangunan) => Variabel Predictor
- Jumlah keluarga dan individu (penduduk) dan jumlah Desil1 (Individu miskin desil 1) => Variabel Predictor
- Efectivitas Label (yes/no) => Variabel Target

  Link Data :
  https://github.com/aisyawina/SquadGirls/blob/main/data1.csv
  
## Algoritma Machine Learning yang Di Pilih
1. CART
   CART (Classification and Regression Tree) dipilih karena cocok digunakan pada data yang kecil dan terstruktur, mampu memberikan performa akurat tanpa memerlukan jumlah
   data besar serta menjelaskan logika klasifikasi fiskal secara jelas. Metode ini juga mudah diinterpretasikan karena memiliki struktur pohon keputusan yang visual dan
   logis, sehingga memudahkan dalam menjelaskan faktor-faktor yang menyebabkan suatu provinsi diklasifikasikan sebagai “efektif” atau “tidak efektif” dalam penggunaan
   anggaran. Selain itu, CART mampu menangani data numerik dan kategorikal hasil encoding tanpa memerlukan asumsi distribusi tertentu seperti normalitas, menjadikannya
   fleksibel untuk analisis data sosial ekonomi.
2. Random Forest
   Random Forest (RF) dipilih karena memberikan performa yang lebih stabil dan akurat dibandingkan CART, dengan membangun banyak pohon dan menggabungkan hasilnya melalui
   teknik bagging. Model ini juga mampu mengukur pentingnya fitur secara kuantitatif (feature importance), sehingga membantu dalam memahami variabel mana yang paling
   berpengaruh dalam klasifikasi. Selain itu, RF tahan terhadap outlier dan variasi data (noise), karena menggunakan banyak pohon, menjadikannya sangat cocok untuk
   menganalisis data sosial ekonomi provinsi yang kompleks
   
## Work Flow
1. CART
   https://github.com/aisyawina/SquadGirls/blob/main/Workflow_CART%20Diagram.png
   
2. Random Forest
  https://github.com/aisyawina/SquadGirls/blob/main/Workflow_Random%20Forest%20(RF)%20Diagram.png

## Detail Coding 
https://github.com/aisyawina/SquadGirls/blob/main/Project_UAS_Kelompok_Squad_Girls.html

## Hasil Akurasi
<img width="262" alt="image" src="https://github.com/user-attachments/assets/5cadf85a-18b6-4f39-834c-f0b7ea62b465" />

Model CART terbukti lebih unggul dalam mengklasifikasikan efektivitas penggunaan anggaran antarprovinsi berdasarkan hasil evaluasi model. Sementara itu, Random Forest cenderung menghasilkan lebih banyak kesalahan klasifikasi, sehingga akurasi dan F1-Score-nya lebih rendah dibandingkan CART menurut confusion matrix. Namun, berdasarkan grafik performa dari 30 kali perulangan, Random Forest (sebagai model ensemble) menunjukkan performa yang lebih stabil karena menggabungkan rata-rata dari banyak model, sedangkan CART sebagai model pohon tunggal lebih sensitif terhadap variasi data.



## Penulis
- Nama kamu

<p align="center">
  <strong>Tulisan ini di tengah</strong>
</p>

<p align="center">
  <img src="https://example.com/logo.png" width="200" alt="Logo Proyek">
</p>

<p align="center">
  <strong>Selamat datang di Proyek Kami!</strong><br>
  Dokumentasi dan sumber terbuka untuk semua.
</p>
