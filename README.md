<p align="center">
 <img src="Data Source/Logo IPB University_Horizontal.png" width=auto height=auto alt="IPB University" />
 <h2 align="center">LAPORAN PRAKTIKUM STATISTIKA MACHINE LEARNING</h2>
<p align="center">Dibuat Oleh: Squad Girls Group</p>


# Optimalisasi Alokasi Fiskal dalam Peningkatan Pembangunan Manusia Menuju Indonesia Emas 2045
## Deskripsi Proyek
Repositori ini merupakan bagian dari tugas akhir mata kuliah Statistika Machine Learning, yang bertujuan menganalisis efektivitas alokasi fiskal antarprovinsi dalam meningkatkan Indeks Pembangunan Manusia (IPM) dan mengentaskan kemiskinan (Desil 1), dalam kerangka visi Indonesia Emas 2045

## Latar Belakang
<p align="JUSTIFY">
Visi Indonesia Emas 2045 menekankan pentingnya pertumbuhan inklusif dan berkelanjutan. Namun, tantangan fiskal nasional yang dihadapi adalah ketimpangan antarprovinsi dalam hal alokasi dan efektivitas penggunaan anggaran. Oleh karena itu, urgensi mengarahkan fiskal ke outcome nyata seperti peningkatan Indeks Pembangunan Manusia (IPM) dan pengentasan kemiskinan menjadi sangat penting. Fakta menunjukan bahwa Distribusi IPM antarprovinsi menunjukkan bahwa sebagian besar provinsi memiliki IPM antara 70–75, namun terdapat beberapa provinsi dengan IPM sangat rendah (<60) dan sangat tinggi (>80). Ini mengindikasikan adanya ketimpangan pembangunan manusia yang cukup tajam antarwilayah. Meskipun ada beberapa wilayah provinsi memiliki alokasi fiskal (PAGU APBN) cukup besar, tidak semua menunjukkan peningkatan signifikan pada IPM. Hal ini menandakan perlunya klasifikasi efektivitas penggunaan anggaran berbasis data sebagai dasar penyusunan kebijakan yang lebih tepat sasaran.
 
</p>

## Tujuan Penelitian
Proyek ini bertujuan untuk:
- Menganalisis hubungan antara alokasi fiskal provinsi, Indeks Pembangunan Manusia (IPM), dan distribusi kelompok miskin Desil 1 di seluruh Indonesia.
- Mengetahui efektivitas penggunaan anggaran, dengan asumsi bahwa jika pagu anggaran tinggi namun IPM tetap rendah, maka penggunaan anggaran tersebut belum optimal dalam
  meningkatkan kesejahteraan manusia.
- Mengklasifikasikan provinsi ke dalam kategori efektif atau tidak efektif dalam penggunaan fiskal, menggunakan pendekatan Tree-Based Classification (CART & Random Forest),
  yang akan dijadikan dasar rekomendasi kebijakan fiskal untuk mewujudkan visi Indonesia Emas 2045.

## Sumber Data Primer
1. Sumber data: Satu Data <a href="https://data.go.id/dataset/dataset/total-apbn-tahun-berjalan"> (data.go.id/APBN_2024)</a> , 
2. Indeks Pembangunan Manusia 2024 (bps.go.id), 
3. Data Demografi Kesejahteraan Masyarakat-Desil 1 (data-go.id)

## Variabel
- PAGU APBN 2024 dan Provinsi (Alokasi fiskal) => Variabel Predictor
- IPM_2024 (Outcome pembangunan) => Variabel Predictor
- Jumlah keluarga dan individu (penduduk) dan jumlah Desil1 (Individu miskin desil 1) => Variabel Predictor
- Efectivitas Label (yes/no) => Variabel Target

  Link Data Sekunder yang sudah digabung :
  <a href="Data Source/data1.csv"> Klik dan Lihat Data Berikut! </a>

  
## Algoritma Machine Learning yang Di Pilih

1. CART
   <p align="JUSTIFY">
   CART (Classification and Regression Tree) dipilih karena cocok digunakan pada data yang kecil dan terstruktur, mampu memberikan performa akurat tanpa memerlukan jumlah
   data besar serta menjelaskan logika klasifikasi fiskal secara jelas. Metode ini juga mudah diinterpretasikan karena memiliki struktur pohon keputusan yang visual dan
   logis, sehingga memudahkan dalam menjelaskan faktor-faktor yang menyebabkan suatu provinsi diklasifikasikan sebagai “efektif” atau “tidak efektif” dalam penggunaan
   anggaran. Selain itu, CART mampu menangani data numerik dan kategorikal hasil encoding tanpa memerlukan asumsi distribusi tertentu seperti normalitas, menjadikannya
   fleksibel untuk analisis data sosial ekonomi.
   </p>
   
3. Random Forest
   <p align="JUSTIFY">
   Random Forest (RF) dipilih karena memberikan performa yang lebih stabil dan akurat dibandingkan CART, dengan membangun banyak pohon dan menggabungkan hasilnya melalui
   teknik bagging. Model ini juga mampu mengukur pentingnya fitur secara kuantitatif (feature importance), sehingga membantu dalam memahami variabel mana yang paling
   berpengaruh dalam klasifikasi. Selain itu, RF tahan terhadap outlier dan variasi data (noise), karena menggunakan banyak pohon, menjadikannya sangat cocok untuk
   menganalisis data sosial ekonomi provinsi yang kompleks
   </p>
   
## Work Flow
CART vs Random Forest
  Project kami memiliki metode penelitian berikut, dimana kami memiliki proses "Data Preparation/Gathering/Collection", "PreProcessing dan Feature Engineering", "Modelling", "Evaluation & Conclusion"
   <p><img src="Workflow/Flowchart CART vs Random Forest.PNG" alt="" width="600px"/></p>
   
## Detail Coding 
Bisa didapatkan teknis coding sesuai urutan workflow di atas pada <a href="Project_UAS_Kelompok_Squad_Gilrs rev 2 (2).ipynb"> file.ipynb </a> berikut


## Hasil Akurasi


<img width="262" alt="image" src="https://github.com/user-attachments/assets/5cadf85a-18b6-4f39-834c-f0b7ea62b465" />

<p align="JUSTIFY">
Model CART terbukti lebih unggul dalam mengklasifikasikan efektivitas penggunaan anggaran antarprovinsi berdasarkan hasil evaluasi model. Sementara itu, Random Forest cenderung menghasilkan lebih banyak kesalahan klasifikasi, sehingga akurasi dan F1-Score-nya lebih rendah dibandingkan CART menurut confusion matrix. Namun, berdasarkan grafik performa dari 30 kali perulangan, Random Forest (sebagai model ensemble) menunjukkan performa yang lebih stabil karena menggabungkan rata-rata dari banyak model, sedangkan CART sebagai model pohon tunggal lebih sensitif terhadap variasi data.
</p>

## Insight

- Features Importance
  
  <img width="262" alt="image" src="Data Source/Features Importances.png" />
  
- Tree Plot

  <img width="262" alt="image" src="Data Source/Tree Plot.png" />


 <p align="JUSTIFY"> 
Model CART menunjukkan bahwa fitur paling dominan dalam klasifikasi adalah IPM, yang menandakan fokus utama pada outcome sosial. Hal ini tercermin dari tree-plot yang menunjukkan pembagian keputusan pertama berdasarkan nilai IPM_2024 dengan threshold 73.08. Sebaliknya, model Random Forest lebih menekankan pada input finansial, dengan PAGU_prov sebagai indikator utama efektivitas kebijakan fiskal, terutama pada provinsi dengan anggaran di bawah 9,1 triliun, sehingga lebih menyoroti besaran alokasi dana dibandingkan hasil sosialnya.
</p>

## Kesimpulan dan Rekomendasi
<p align="JUSTIFY">
Berdasarkan temuan, anggaran besar tidak selalu berbanding lurus dengan peningkatan kualitas hidup (IPM), terbukti dari beberapa provinsi dengan alokasi anggaran besar namun dikategorikan tidak efektif. Model CART dinilai lebih cocok untuk mengevaluasi efektivitas jangka pendek berdasarkan IPM, sementara Random Forest lebih sesuai untuk tujuan jangka panjang karena stabil dan tidak bias terhadap daerah kaya. Penggunaan model statistik berbasis machine learning disarankan untuk mendukung pengambilan keputusan yang lebih akurat dan tepat sasaran. Pemerintah direkomendasikan memprioritaskan daerah dengan IPM rendah dan jumlah penduduk miskin tinggi untuk mengejar ketertinggalan pembangunan.
</p>

## PPT 
Presentasi dalam bentuk power point dapat dilihat disini :

https://bit.ly/3Hen38x


## Laporan Akhir

https://bit.ly/3HrbSJF



## Reels di Sosmed
Bantu likes and comment ya gaes :)


https://www.instagram.com/reel/DKHXXPWSacL/?igsh=MWp2NnU2ZmhuajJuZg==

## Video 
link video dapat dilihat di sini :

https://bit.ly/4ktMzow


## Penulis
- Riza Rahmah Angelia ( M0501241008 )
- Aisya Wina Wahda (M0501241053)
- Latifah Zahra (M0501241075)
- Sely F Wakhidah (M0501241038) 


<p align="center">
  <strong>Selamat datang di Proyek Kami!</strong><br>
  Dokumentasi dan sumber terbuka untuk semua.
</p>
