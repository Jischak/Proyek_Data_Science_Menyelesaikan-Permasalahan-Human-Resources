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

Pada proyek ini, Anda dapat menggunakan berbagai IDE seperti Jupyter Notebook atau Google Colaboratory (Google Colab). Apabila, Anda menjalankan latihan ini melalui Jupyter Notebook, maka ikuti langkah setup environment dibawah ini:
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
pip install numpy pandas matplotlib seaborn jupyter scikit-learn==1.2.2
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
https://docs.google.com/spreadsheets/d/1c_3Th8-2sbVCJe6vJvhG48uSjxX9n8ExNBIZqhRrZQY/edit?usp=sharing
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

```

## Conclusion
Berikut ini konklusi dari proyek ini:
1. Jumlah karyawan yang keluar dari Perusahaan Jaya Jaya Maju adalah sebanyak 179 orang dari total 1058 karyawan atau apabila dipresentasekan sebanyak 16,9%.
2. Beberapa faktor yang mempengaruhi karyawan untuk keluar dari perusahaan antara lain:
> a. Jarak tempat tinggal ke kantor: Karyawan yang memiliki jarak tempat tinggal ke kantor antara 0-5 Km dominan untuk keluar dari perusahaan, dimana pada kasus ini sebanyak 72 orang.
> b. Total Lama Bekerja: Karyawan yang memiliki total bekerja selama 10 tahun (0-10 tahun) cenderung lebih besar untuk keluar dari perusahaan dibanding total lama bekerja 10-20 tahun, 20-30 tahun, >40 tahun. Kontribusi-nya sebanyak 137 orang.
> c. Keterlibatan dalam Pekerjaan: Karyawan yang memiliki keterlibatan tinggi (high) dalam pekerjaan memiliki presentase untuk keluar dari perusahaan lebih tinggi (sebanyak 51,4%) dari pada yang keterlibatannya sedang (medium), rendah (low), dan sangat tinggi (very high).
> d. Tingkat Pekerjaan (rendah - tinggi / 1 - 5): Tingkat pekerjaan yang rendah memiliki kontribusi tertinggi untuk jumlah karyawan yang keluar dengan jumlah sebanyak 108 orang.
> e. Kepuasan Lingkungan Kerja: Karyawan yang keluar cenderung memiliki kepuasan yang rendah (low) di lingkungan bekerjanya, dengan presentase sebanyak 31,8%.
> f. Kepuasan Pekerjaan: Keryawan yang keluar cenderung memiliki kepuasan akan pekerjaannya yang tinggi (high), hal ini didukung dengan presentase sebanyak 34,6%.
> g. Tingkat Performa: Jumlah karyawan yang keluar namun memiliki tingkat performa tinggi (151 orang) lebih banyak signifikan dibandingkan yang memiliki tingkat performa yang rendah (28 orang).
> h. Kepuasan Hubungan Kerja: Karyawan yang keluar cederung memiliki kepuasan hubungan kerja yang sangat tinggi (very high) yaitu dengan presentase sebanyak 29,1%. Disisi lain, untuk karyawan dengan kepuasan hubungan kerja tinggi (high) dan rendah (low) memiliki presentase yang tidak berbeda jauh daripada kepusasan hubungan kerja yang sangat tinggi (very high) dengan masing-masing memiliki presentase 27,4% dan 25,7%.
> i. Keseimbangan Kehidupan Kerja: Karyawan yang keluar didominasi oleh para karyawan yang memiliki keseimbangan kehidupan kerja yang sangat baik (excellent) dengan jumlah karyawan sebanyak 94 orang. Disisi lain, karyawan yang keluar dengan keseimbangan kehidupan kerja baik (good), luar biasa (outstanding), dan rendah (low) memiliki jumlah masing-masing adalah 45, 22, dan 18 orang.
3. Dari 179 orang yang keluar dari perusahaan, dominan memiliki umur 31 tahun. Hal ini didukung dengan jumlah karyawan yang keluar adalah sebanyak 14 orang.
4. Berdasarkan peran pekerjaan karyawan yang keluar dari perusahaan terbanyak tergolong dalam peran pekerjaan sebagai Laboratory Technician dengan jumlah sebanyak 49 orang.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- action item total lama bekerja di hire yang sdh >10 tahun
- action item keterlibatan dalam pekerjaan cb ke open ai
- action item kepuasan lingkungan kerja dicari tahu alasanya mengapa dan diperbaiki
- action item kepuasan pekerjaan ini apakah ada opportunity lebih baik / faktir internal seperti lingkungan kerja
- action item mengapa sangat baik keseimbangan kehidupan kerja tapi paling banyak keluar
- action item cek pekerjaan laboratory hubunkan dengan faktor lainnya
- tinggi tapi keluar: keterlibatan dlm pekerjaan, kepuasan pekerjaan
- sangat tinggi tapi keluar: kepuasan hubungan kerja
