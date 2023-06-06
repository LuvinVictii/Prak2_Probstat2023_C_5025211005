# Praktikum 2 Probstat 2023 Kelas C 5025211005

<div align=center>
Muhammad Daffa Harits

5025211005

Probstat Kelas C
  
</div>

## No 1

### A.
Carilah Standar deviasi dari data selisih pasangan pengamatan tabel diatas!

![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/74f9a254-1d6b-44ca-b511-de4e569dcce7)

### B.
Carilah nilai t (p-value)!

![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/3a4177af-ec0f-4d87-a972-8b98ccddf189)

### C. 
Tentukanlah apakah terdapat pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen, sebelum dan sesudah melakukan aktivitas 𝐴 jika diketahui tingkat signifikansi 𝛼 = 5% serta H0 : “tidak ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen sebelum dan sesudah melakukan aktivitas 𝐴”!
```
H0 : “Tidak ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴”
H1 : “Ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴”

Conf lvl = 95% = 0.95
Signif lvl (𝛼) = 5% = 0,05 

Lihat Tabel distribusi t, two tail
Kolom = 𝛼/2 = 0,05/2 = 0,025
Baris = df = 8 
Crit value = 2,306
t = 7.7152
7.7152, tolak H0
Sehingga kesimpulannya sesuai dengan H1 atau Ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴

(Significant Level) = 5% = 0,05 (Significant Level)
p-value = 5.664e-05 = 0,00005664
0,00005664 <= 0,05
p-value <= 𝛼, tolak H0
Sehingga kesimpulannya sesuai dengan H1 atau Ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴
```
## No. 2

### A.
Apakah Anda setuju dengan klaim tersebut? Jelaskan!
```
Karena n >= 30 maka dapat digunakan distribusi normal dengan uji z-distribution. Menggunakan fungsi `zsum.test()` dan menggunakan data yang diketahui sebagai berikut : R zsum.test(mean.x = 23500, sigma.x = 3000, n.x = 100, alternative = "greater", mu = 25000, conf.level = 0.95)
```
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/c8b82501-603c-47ff-b64c-337c4e1e48cf)
```
Berdasarkan hasil yang telah didapatkan, H1 bernilai salah bahwa Rata-rata mobil dikemudikan kurang dari 25.000 kilometer per tahun Saya tidak setuju dengan klaim tersebut.
```

### B. 
Buatlah kesimpulan berdasarkan p-value yang dihasilkan!
```
Karena p-value(z=-5) > (α=0.05) , maka H0 diterima atau berada pada daerah penerimaan. Sehingga, kesimpulannya Hipotesis Alternatif (H1) bernilai bernilai salah atau menolak H1 bahwa Rata-rata mobil dikemudikan lebih dari 25.000 kilometer per tahun
```

## No. 3

### A.
Menentukan Hipotesis
```
HO : Tidak ada perbedaan pada rata-rata saham kota Bandung (µ1) dengan rata-rata saham Kota Bali (µ2).
H1 : Ada perbedaan pada rata-rata saham kota Bandung (µ1) dengan rata-rata saham Kota Bali (µ2).
```

### B. 
Hitung sampel statistik
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/50e4ec43-f6f8-4e6f-b4c9-1609cdf91f96)

### C.
Lakukan uji statistik (df = 2)
```
Menggunakan plotDist(dist = 't', df = 2, col = "blue")
```
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/857bdac0-9bd1-4bfa-ab71-497dfcd68903)

### D.
Nilai kritikal
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/619cc619-eeb1-43f6-8331-66b9439e97b1)

### E.
Keputusan
```
t = 1.8304 dan nilai kritikal = 2.073873
t < nilai kritikal, atau t berada pada daerah penerimaan H0 (TERIMA H0)

p-value = 0.07381 dan α = 0.05
p-value >= α

Jadi keputusannya adalah menerima Hipotesis null atau H0.
```

### F.
Kesimpulan
```
Berdasarkan keputusan pada no. 3e, maka kesimpulannya adalah
"Menerima Hipotesis null atau H0 bahwa Tidak ada perbedaan pada rata-rata saham kota Bandung (µ1) dengan rata-rata saham Kota Bali (µ2). µ1 = µ2"
```

## No. 4

### A.
Buatlah plot sederhana untuk visualisasi data.
```
GlassTempLight <- read_csv("C:/Users/admin/Downloads/GTL.csv")

install.packages("ggplot2")
library(ggplot2)

ggplot(GlassTempLight, aes(x = Temp, y = Light)) + 
  geom_point() + 
  facet_grid(.~Glass, labeller = label_both)
```
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/75da5743-38dc-414c-8916-c79ce2a85aa8)

### B.
Lakukan uji ANOVA dua arah.
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/e6bc8e4e-6281-4fc0-a963-a899dfa5999c)

### C.
Tampilkan tabel dengan mean dan standar deviasi keluaran cahaya untuk setiap perlakuan (kombinasi kaca pelat muka dan suhu operasi).
```
install.packages("dplyr") #instal paket dplyr
library(dplyr) #memuat paket dplyr

SummaryData <- group_by(GlassTempLight, Glass, Temp) %>%
  summarise(mean=mean(Light), sd=sd(Light)) %>%
  arrange(desc(mean))
print(SummaryData)
```
![image](https://github.com/LuvinVictii/Prak2_Probstat2023_C_5025211005/assets/78089862/f04c123a-d70e-4253-8514-c292f1953d99)
