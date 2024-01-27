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

Link Pertanyaan + Jawaban: https://docs.google.com/spreadsheets/d/1c_3Th8-2sbVCJe6vJvhG48uSjxX9n8ExNBIZqhRrZQY/edit?usp=sharing

### Bagaimana proses membuat business dashboard dalam proyek ini?
Business dashboard menggunakan dataset yang telah melalui tahapan persiapan. Dataset tersebut di ekspor dalam format csv dari notebook.ipynb dan setelah itu di import ke dalam Looker Studio. Selain itu, pada looker studio ada penyesuaian dan modifikasi tipe data pada beberapa variabel. Disisi lain, terdapat juga penambahan dibuat penambahan beberapa variabel baru untuk kebutuhan visualisasi di dashboard.

Link business dashboard: https://lookerstudio.google.com/reporting/f96f16b9-6803-49ad-925e-1d2334a12917

### Deskripsi Business Dashboard
Jelaskan tentang business dashboard yang telah dibuat. 


## Menjalankan Sistem Machine Learning
Jelaskan cara menjalankan protoype sistem machine learning yang telah dibuat. Selain itu, sertakan juga link untuk mengakses prototype tersebut.

```

```

## Conclusion
Jelaskan konklusi dari proyek yang dikerjakan.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- action item 1
- action item 2
