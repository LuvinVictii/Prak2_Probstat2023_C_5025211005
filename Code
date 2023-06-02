# No 1.)

# a.
# Input data:
X <- c(78,75,67,77,70,72,78,70,77)
Y <- c(100,95,70,90,90,90,89,90,100)
# Selisih X dan Y
diff <- c(Y-X)
# Standar Defiasi
SD <- sd(diff)
paste("Standar Deviasi = ", SD)

# b.
t.test (Y, X, paired = TRUE, var.equal = FALSE) 

# c. 
#H0 : “Tidak ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴”
#H1 : “Ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴”

#Conf lvl = 95% = 0.95
#Signif lvl (𝛼) = 5% = 0,05 

# Lihat Tabel distribusi t, two tail
# Kolom = 𝛼/2 = 0,05/2 = 0,025
# Baris = df = 8 
# Crit value = 2,306
# t = 7.7152
# 7.7152, tolak H0
# Sehingga kesimpulannya sesuai dengan H1 atau Ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴

#𝛼(Significant Level) = 5% = 0,05 (Significant Level)
# p-value = 5.664e-05 = 0,00005664
# 0,00005664 <= 0,05
# p-value <= 𝛼, tolak H0
# Sehingga kesimpulannya sesuai dengan H1 atau Ada pengaruh yang signifikan secara statistika dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan aktivitas 𝐴


# No 2.)

install.packages("BSDA")
library(BSDA)
# H0: "Rata-rata mobil dikemudikan <= 25.000 kilometer per tahun."
# H1: "Rata-rata mobil dikemudikan > 25.000 kilometer per tahun."
# mean = 23500 = mean.x
# SD = 3000 = sigma.x
# n = 100 = n.x
# H1 = lebih besar dari = greater =(alternative)
# mu = 25000 
# conf lvl = 95% = 0,95 = conf.level
# signif lvl (α)= 5% = 0,05

# a.
# kn >= 30 --> distribusi normal dengan uji z-distribution :
zsum.test(mean.x = 23500, sigma.x = 3000, n.x = 100, alternative = "greater", mu = 25000, conf.level = 0.95)  
# Berdasarkan hasil yang telah didapatkan, terima H0

# c.
# p-value(z=-5) > (α=0.05)
# Berada pada daerah penerimaan H0.
# Sehingga, kesimpulannya Hipotesis Alternatif (H1) bernilai salah atau menolak H1 bahwa Rata-rata mobil dikemudikan lebih dari 25.000 kilometer per tahun


# No 3.)

# a.
# HO: "Tidak ada perbedaan pada rata-rata saham kota Bandung (µ1) dengan rata-rata saham Kota Bali (µ2)"
# H1: "Ada perbedaan pada rata-rata saham kota Bandung (µ1) dengan rata-rata saham Kota Bali (µ2)"

# b.
n_bandung <- 20
n_bali <- 27
mean_bandung <- 3.64
mean_bali<- 2.79
sd_bandung <- 1.67
sd_bali <- 1.5
confident_level <- 0.95
tsum.test(mean.x=mean_bandung, s.x = sd_bandung, n.x = n_bandung, 
          mean.y =mean_bali , s.y = sd_bali, n.y = n_bali, 
          alternative = "two.side", var.equal = TRUE, conf.level = confident_level)

# c.
install.packages("vctrs")
install.packages("mosaic")
install.packages("ggforce")
library(mosaic)

plotDist(dist = 't', df = 2, col = "black")

# d.
qt(p=0.05/2, df=22, lower.tail=FALSE)

# e.
# Berdasarkan hasil yang didapatkan sebelumnya :
# t = 1.8304
# crit val = 2.073873
# t < crit val, atau t berada pada daerah penerimaan H0

# p-value = 0.07381
# α = 0.05
# p-value >= α (TERIMA H0)

# Keputusannya adalah menerima Hipotesis null atau H0


# f.
# Kesimpulannya:
# Tidak ada perbedaan pada rata-rata saham kota Bandung (µ1) dengan rata-rata saham Kota Bali (µ2)
# µ1 = µ2


# No 4.)

install.packages("readr")
library(readr)

# a.
GlassTempLight <- read_csv("C:/Users/admin/Downloads/GTL.csv")

install.packages("ggplot2")
library(ggplot2)

ggplot(GlassTempLight, aes(x = Temp, y = Light)) + 
  geom_point() + 
  facet_grid(.~Glass, labeller = label_both)

# b.
GlassTempLight $Glass <- as.factor(GlassTempLight $Glass)
GlassTempLight $Temp_Factor <- as.factor(GlassTempLight $Temp)
str(GlassTempLight)

anova <- aov(Light ~ Glass*Temp_Factor, data = GlassTempLight)
summary(anova) 

# c.
install.packages("dplyr") #instal paket dplyr
library(dplyr) #memuat paket dplyr

SummaryData <- group_by(GlassTempLight, Glass, Temp) %>%
  summarise(mean=mean(Light), sd=sd(Light)) %>%
  arrange(desc(mean))
print(SummaryData)

