# Proyek Akhir: Menyelesaikan Permasalahan Human Resources


## Business Understanding
Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. 

### Permasalahan Bisnis
Sebagai perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan.
Hal ini berimbas tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

### Cakupan Proyek
<p>Untuk menjawab permasalahan bisnis tersebut, kita akan mengidentifikasi berbagai faktor yang mempengaruhi tingginya attrition rate. Nah, pada proyek ini kita akan membuat bussiness dashboard untuk membantu memonitori berbagai faktor tersebut. 
</p>

<p>Selain itu, kita akan menerapkan analisis klasifikasi untuk attrition dengan metode machine learning. Algoritma machine learning yang digunakan akan disesuaikan dengan keadaan dataset (akan ditentukan pada tahapan modeling). Kita juga akan melakukan sedikit proses Exploratory Data Analysis (EDA) untuk memperoleh gambaran terkait dataset yang akan kita gunakan. Pada prosesnya, kita juga akan coba melihat karakteristik dari setiap kelompok data (berdasarkan beberapa kolom kategoris) yang terdapat dalam dataset. 
</p>

Nah, berdasarkan cakupan proyek tersebut, kita membutuhkan beberapa resource dan tool, yaitu

1. data karyawan di perusahaan (employee_data).
2. Tool yang digunakan untuk membuat bussiness dashboard adalah Looker Studio.
3. bahasa pemrograman Python sebagai tool utama kita dalam proyek ini.
4. berbagai library pendukung untuk pengolahan data dan pengembangan model machine learning.

### Persiapan

Sumber data: https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee

Konteks data:
  - EmployeeId - ID karyawan
  - Attrition - Apakah ada pengurangan karyawan? (0=tidak, 1=ya)
  - Age - Umur karyawan
  - BusinessTravel - Perjalanan Bisnis yang dilakukan untuk perkerjaan
  - DailyRate - Gaji Harian dari karyawan
  - Department - Department dimana karyawan bekerja
  - DistanceFromHome - Jarak dari tempat bekerja ke rumah (km)
  - Education - 1-Below College, 2-College, 3-Bachelor, 4-Master,5-Doctor
  - EducationField - Bidang pendidikan
  - EnvironmentSatisfaction - 1-Low, 2-Medium, 3-High, 4-Very High
  - Gender - Jenis Kelamin
  - HourlyRate - Gaji per jam
  - JobInvolvement - 1-Low, 2-Medium, 3-High, 4-Very High
  - JobLevel - Level dari pekerjaan (1 sampai 5)
  - JobRole - Jabatan
  - JobSatisfaction - 1-Low, 2-Medium, 3-High, 4-Very High
  - MaritalStatus - Status Pernikahan
  - MonthlyIncome - Pendapatan perbulan
  - MonthlyRate - Gaji perbulan
  - NumCompaniesWorked - Jumlah perusahaan tempat bekerja
  - Over18 - Umur diatas 18 Tahun?
  - OverTime - Lembur?
  - PercentSalaryHike - Persentase kenaikan gaji tahun lalu
  - PerformanceRating - 1-Low, 2-Good, 3-Excellent, 4-Outstanding
  - RelationshipSatisfaction - 1-Low, 2-Medium, 3-High, 4-Very High
  - StandardHours - Jam Kerja Standar
  - StockOptionLevel - Tingkat Opsi Saham
  - TotalWorkingYears - Jumlah Total tahun bekerja
  - TrainingTimesLastYear - Jumlah pelatihan yang diikuti tahun lalu
  - WorkLifeBalance - 1-Low, 2-Good, 3-Excellent, 4-Outstanding
  - YearsAtCompany - Lama di Perusahaan (Tahun)
  - YearsInCurrentRole - Lama di posisi saat ini (Tahun)
  - YearsSinceLastPromotion - Tahun sejak promosi terakhir (Tahun)
  - YearsWithCurrManager - Lama bekerja dengan manajer saat ini (Tahun)

Proyek ini dibuat melalaui Google Colaboratory (Google Colab). Namun Anda dapat menjalankan proyek ini juga melalui Jupyter Notebook, maka ikuti langkah setup environment dibawah ini:
Setup environment menggunakan conda:
  1. Buka terminal atau PowerShell
  2. Jalankan perintah berikut untuk membuat environment baru
  ```
  conda create --name employee-classification-project python=3.9
  ```
  3. Aktifkan virtual environment dengan menjalankan perintah berikut
  ```
  conda activate employee-classification-project
  ```
  4. Instal semua library yang dibutuhkan dengan perintah berikut.
  ```
  pip install -r requirements.txt
  ```
  5. Buka jupyter-notebook dengan menjalankan perintah berikut.
  ```
  jupyter-notebook .
  ```


## Business Dashboard

### Apa yang ingin diketahui?
Dalam proyek ini, business dashboard yang dibuat untuk memonitori data attrition. Berikut beberapa pertanyaan yang akan kita cari jawabannya dalam proyek ini.

Link Pertanyaan + Jawaban: 
```
https://docs.google.com/spreadsheets/d/1yPehiJPaGXvJkE0lcKWCbZ_x6Q9Nbfdvr7pveI_u7Ic/edit?usp=sharing
```

### Bagaimana proses membuat business dashboard dalam proyek ini?
Business dashboard menggunakan dataset yang telah melalui tahapan persiapan. Dataset tersebut di ekspor dalam format csv dari notebook.ipynb dan setelah itu di import ke dalam Looker Studio. Selain itu, pada looker studio ada penyesuaian dan modifikasi tipe data pada beberapa variabel. Disisi lain, terdapat juga penambahan dibuat penambahan beberapa variabel baru untuk kebutuhan visualisasi di dashboard.

Link business dashboard: 
```
https://lookerstudio.google.com/reporting/f96f16b9-6803-49ad-925e-1d2334a12917
```

### Deskripsi Business Dashboard

#### Dashboard Karyawan Jaya Jaya Maju - Attrition
Business dashboard ini berisi visualisasi data dari variabel-variabel yang mempengaruhi attrition. Dimana, tampilan awal menunjukan keselurhan data. Namun, apabila kita ingin melihat data yang tegolong dalam attrition maka dapat dilakukan filter. Untuk data attrition, kita dapat memberi nilai 1 pada menu filter yang terdapat di bagian kanan atas. Sebaliknya, untuk yang data yang tidak tergolong attrition maka kita dapat memberi nilai 0.  

![dashboard attrition](https://github.com/Jischak/Proyek_Data_Science_Menyelesaikan-Permasalahan-Human-Resources/assets/52368239/de5c573d-3e0b-4c19-909a-3f38eaf34e45)



## Menjalankan Sistem Machine Learning
Berikut ini cara untuk menjalankan prototype Machine Learning untuk prediksi Attrition Karyawan di Jaya Jaya Maju.
Prototype ini bisa dicoba baik secara lokal (offline) maupun online. 
![image](https://github.com/Jischak/Proyek_Data_Science_Menyelesaikan-Permasalahan-Human-Resources/assets/52368239/52dd90f3-4e6a-4d91-99d5-e94bc36ac2c7)

### Bagaiamana mencoba prototype secara lokal?
  1. Buka terminal atau PowerShell
  2. Aktifkan virtual environment yang telah dibuat sebelumnya
  ```
  conda activate employee-classification-project
  ```
  3. Masuk ke lokasi dimana file streamlit (prediksi.py) berada
  4. Jalankan file streamlit dengan perintah berikut ini:
  ```
  streamlit run prediksi.py
  ```

### Bagaiamana mencoba prototype secara online?
Tentunya, mudah kok... kamu bisa mengakses melalui link dibawah ini:
```
https://proyekdatasciencemenyelesaikan-permasalahan-human-resources-uq.streamlit.app/
```

## Conclusion
Berikut ini konklusi dari proyek ini:
  1. Jumlah karyawan yang keluar dari Perusahaan Jaya Jaya Maju adalah sebanyak 179 orang dari total 1058 karyawan atau apabila dipresentasekan sebanyak 16,9%.
  2. Beberapa faktor yang mempengaruhi karyawan untuk keluar dari perusahaan antara lain:
     - Jarak tempat tinggal ke kantor: Karyawan yang memiliki jarak tempat tinggal ke kantor antara 0-5 Km dominan untuk keluar dari perusahaan, dimana pada kasus ini sebanyak 72 orang.
     - Total Lama Bekerja: Karyawan yang memiliki total bekerja selama 10 tahun (0-10 tahun) cenderung lebih besar untuk keluar dari perusahaan dibanding total lama bekerja 10-20 tahun, 20-30 tahun, >40 tahun. Kontribusi-nya sebanyak 137 orang.
     - Keterlibatan dalam Pekerjaan: Karyawan yang memiliki keterlibatan tinggi (high) dalam pekerjaan memiliki presentase untuk keluar dari perusahaan lebih tinggi (sebanyak 51,4%) dari pada yang keterlibatannya sedang (medium), rendah (low), dan sangat tinggi (very high).
     - Tingkat Pekerjaan (rendah - tinggi / 1 - 5): Tingkat pekerjaan yang rendah memiliki kontribusi tertinggi untuk jumlah karyawan yang keluar dengan jumlah sebanyak 108 orang.
     - Kepuasan Lingkungan Kerja: Karyawan yang keluar cenderung memiliki kepuasan yang rendah (low) di lingkungan bekerjanya, dengan presentase sebanyak 31,8%.
     - Kepuasan Pekerjaan: Keryawan yang keluar cenderung memiliki kepuasan akan pekerjaannya yang tinggi (high), hal ini didukung dengan presentase sebanyak 34,6%.
     - Tingkat Performa: Jumlah karyawan yang keluar namun memiliki tingkat performa tinggi (151 orang) lebih banyak signifikan dibandingkan yang memiliki tingkat performa yang rendah (28 orang).
     - Kepuasan Hubungan Kerja: Karyawan yang keluar cederung memiliki kepuasan hubungan kerja yang sangat tinggi (very high) yaitu dengan presentase sebanyak 29,1%. Disisi lain, untuk karyawan dengan kepuasan hubungan kerja tinggi (high) dan rendah (low) memiliki presentase yang tidak berbeda jauh daripada kepusasan hubungan kerja yang sangat tinggi (very high) dengan masing-masing memiliki presentase 27,4% dan 25,7%.
     - Keseimbangan Kehidupan Kerja: Karyawan yang keluar didominasi oleh para karyawan yang memiliki keseimbangan kehidupan kerja yang sangat baik (excellent) dengan jumlah karyawan sebanyak 94 orang. Disisi lain, karyawan yang keluar dengan keseimbangan kehidupan kerja baik (good), luar biasa (outstanding), dan rendah (low) memiliki jumlah masing-masing adalah 45, 22, dan 18 orang.
  4. Dari 179 orang yang keluar dari perusahaan, dominan memiliki umur 31 tahun. Hal ini didukung dengan jumlah karyawan yang keluar adalah sebanyak 14 orang.
  5. Berdasarkan peran pekerjaan karyawan yang keluar dari perusahaan terbanyak tergolong dalam peran pekerjaan sebagai Laboratory Technician dengan jumlah sebanyak 49 orang.

### Rekomendasi Action Items
Berikut ini beberapa rekomendasi action items yang harus dilakukan oleh perusahaan:
  1. Dalam perekrutan karyawan baru dapat disarankan untuk mengambil karyawan yang telah memiliki total lama bekerja selama 10 tahun.
  2. Memperbaiki lingkungan kerja dengan mencari alasan spesifiknya, seperti:
     - Apabila terkait fasilitas perusahaan dapat meninjau dan perbaiki kondisi fasilitas
     - Memperbaiki hubungan Atasan-Bawahan dengan memberikan pelatihan manajemen untuk meningkatkan keterampilan kepemimpinan dan hubungan antara atasan dan bawahan.
     - Melakukan Komunikasi Terbuka dan Jelas dengan menyelenggarakan pertemuan rutin atau forum terbuka
     - Membuat program Pengembangan Karyawan sebagai peluang untuk pengembangan keterampilan dan pertumbuhan karir
     - Memberi Pengakuan dan Apresiasi melalui implementasi program pengakuan karyawan, seperti penghargaan atau ucapan terima kasih berkala.
  3. Kepuasan pekerjaan yang tinggi, namun dominan karyawan memilih untuk keluar, berikut ini action itemnya:
     - Melakukan exit interview mendalam dengan karyawan yang memutuskan untuk keluar walaupun memiliki kepuasan pekerjaan yang tinggi.
     - Meninjau dan mengevaluasi peluang pengembangan karir yang tersedia bagi karyawan.
     - Menyediakan lebih banyak program pengembangan keterampilan dan pelatihan untuk meningkatkan keahlian karyawan.
     - Meningkatkan program pengakuan dan apresiasi untuk memastikan karyawan merasa dihargai.
     - Melakukan evaluasi faktor-faktor lingkungan kerja seperti hubungan antar rekan kerja, budaya perusahaan, dan manajemen.
     - Meninjau kebijakan kompensasi dan pastikan bahwa mereka kompetitif dengan industri.
  4. Karyawan yang keluar dominan memiliki work-life balance yang sangat baik, action itemnya adalah:
     - Melakukan exit interview mendalam dengan karyawan yang meninggalkan perusahaan untuk memahami alasan mereka meskipun memiliki work-life balance yang baik.
     - Meninjau dan mengevaluasi faktor-faktor kesejahteraan dan kepuasan karyawan selain work-life balance secara rutin.
     - Berikan perhatian khusus pada program pengembangan karir dan peluang pertumbuhan.
     - Konsultasikan dengan karyawan yang masih aktif mengenai pengalaman mereka dengan work-life balance dan apa yang dapat ditingkatkan.
     - Tingkatkan keterbukaan komunikasi antara manajemen dan karyawan untuk memahami kebutuhan mereka secara lebih baik.
     - Tinjau dan evaluasi budaya perusahaan untuk memastikan bahwa nilai-nilai dan praktik perusahaan mendukung work-life balance.
  5. Berikut ini action item yang perlu dilakukan terkait fenomena karyawan yang keluar namun memiliki keterlibatan dalam pekerjaan yang tinggi:
     - Melakukan exit interview yang mendalam untuk memahami alasan karyawan meninggalkan perusahaan meskipun memiliki tingkat keterlibatan tinggi.
     - Meninjau kebijakan dan praktik manajemen untuk memastikan bahwa karyawan merasa didukung dan diakui.
     - Meningkatkan komunikasi internal untuk memastikan karyawan merasa terhubung dan diberi informasi secara jelas.
     - Mengimplementasikan program pengakuan dan penghargaan yang secara aktif menghargai kontribusi karyawan.
     - Fokus pada menciptakan lingkungan kerja yang inklusif dan mendukung kolaborasi.
     - Pertimbangkan kebijakan fleksibilitas kerja untuk memberikan karyawan lebih banyak kendali atas jadwal mereka.
  6. Apa saja action items yang dapat dilakukan dalam menyikapi fenomena karyawan yang dominan keluar walaupun memiliki kepuasan hubungan yang sangat tinggi?
     - Melakukan exit interview yang mendalam untuk memahami dengan lebih baik alasan karyawan meninggalkan perusahaan meskipun memiliki kepuasan hubungan kerja yang sangat tinggi.
     - Meninjau faktor-faktor eksternal yang mungkin memengaruhi keputusan karyawan, seperti tawaran pekerjaan dari perusahaan lain atau perubahan kondisi pribadi.
     - Menyediakan peluang pengembangan karir dan pertumbuhan yang jelas untuk mendorong karyawan tetap di perusahaan.
     - Meninjau gaya kepemimpinan di berbagai tingkatan organisasi untuk memastikan bahwa karyawan merasa didukung dan dihargai.
     - Meningkatkan program penghargaan dan pengakuan untuk menunjukkan apresiasi terhadap kontribusi karyawan.
