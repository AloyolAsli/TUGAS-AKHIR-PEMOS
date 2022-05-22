# TUGAS-AKHIR-PEMOS

Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi 2022 oleh Kelompok 1 Oseanografi 2020. Repositori ini memuat materi dan persamaan dari modul 1-4, yaitu Persamaan Adveksi-Difusi 1 Dimensi dan 2 Dimensi, serta Model Hidrodinamika 1 Dimensi dan 2 Dimensi. _Script_ yang dibuat dalam repositori ini menggunakan bahasa _python_ menggunakan _platform Jupyter Notebook_. _Library_ yang digunakan meliputi _numpy, matplotlib_, serta tambahan data gelombang dari _National Buoy Data Center_ (NDBC) melalui _website_ (https://www.ndbc.noaa.gov/obs.shtml). Seluruh _script_ ini merupakan hasil dari kerja Kelompok 1 Oseanografi 2020.
Terima kasih dan semoga bermanfaat!

# ANGGOTA KELOMPOK 1
1. Aloysius Dimas Sanjaya Saliyo          26050120130056  Oseanografi A

2. Fairus Jamil Rizqullah

3. Dafina Amadita Shaquilla               26050120140168  Oseanografi A

4. Vanessa Kurniawan

5. Khana Nadira Sastradjaja               26050120140166  Oseanografi B

6. Bagas Priambodo

7. Priska E. Lumban Batu

8. Laurentia Levina Pramestanti           26050120140126 Oseanografi B



# MODUL 1. PERSAMAAN ADVEKSI-DIFUSI 1 DIMENSI




# MODUL 2. PERSAMAAN ADVEKSI-DIFUSI 2 DIMENSI
**LANGKAH PENGERJAAN:**

```
import matplotlib.pyplot as plt
import numpy as np
import sys
```
```
def percentage(part, whole):
 percentage = 100 * float(part)/float(whole)
 return str(round(percentage,2)) + "X"
 ```

**Memasukkan Nilai Parameter**
```
#Memasukkan Parameter Awal
C = 0.86 #Kecepatan Aliran
ad = 1.86 #Koefisien Difusi
#Arah Arus (Berdasarkan Geographic Convention)
theta = 86 #Skenario I
#Parameter Lanjutan
q = 0.95 #Kriteria Kestabilan
x = 300 #Jumlah Grid Horizontal (x)
y = 300 #Jumlah Grid Vertikal (y)
dx = 3
dy = 3
Tend = 108 #Lama Simulasi
#Tend = 1
dt = 0.5
#Polutan
px = 150 #Polutan pada grid x
py = 138 #Polutan pada grid y
Ic = 568 #Jumlah Polutan
```

**Perhitungan Energi (U) dan Kecepatan (V) Polutan**
```
#Perhitungan U dan V
u = C * np.sin(theta*np.pi/180)
v = C * np.cos(theta*np.pi/180)
dt_count = 1/((abs(u)/(q*dx))+(abs(v)/(q*dy))+(2*ad/(q*dx*2))+(2*ad/(q*dy*2)))
```

**Pembuatan Grafik**
Menentukan jumlah dan arah jalan polutan serta banyaknya _time series _
```
Nx = int(x/dx) #number of mesh in x direction
Ny = int(y/dy) #number of mesh in y direction
Nt = int(Tend/dt) #number of timesteps
#Perhitungan Titik Polutan di Buang
px1 = int(px/dx)
py1 = int(py/dy)
```


PEMBAHASAN:
1. Analisis Hasil Grafik Yang Didapat
   Berdasarkan pengolahan data yang dilakukan sebelumnya terlihat bahwasannya persebaran polutan yang ada pada scenario di skema 1, skema 2, skema 3, dan skema 4 hanya memiliki perbedaan pada arah persebarannya saja. Hal ini dikarenakan pada scenario di skema 1, skema 2, skema 3, dan skema 4 memiliki nilai theta yang berbeda-beda. Namun jika dilihat secara seksama, keempat skema tersebut memiliki beberapa karakteristik yang dapat dikatakan sama, dimana pada awal terlihat polutan tersebut sangat pekat berada pada suatu titik hingga lama kelamaan mulai tersebar namun memiliki konsentrasi yang menurun. Hal ini disebabkan persebaran polutan dipengaruhi oleh angin dan arus. Hal ini diperkuat oleh Adriani (2020), dimana angin merupakan faktor pembawa polutan dalam menyebarkan polutan ke tempat lain. Angin tersebut turut ikut berpengaruh terhadap konsentrasi polutan yang ada di perairan.

3. Pengaplikasian Dari Persamaan Adveksi-Difusi 2 Dimensi 

# MODUL 3. MODEL HIDRODINAMIKA 1 DIMENSI

# MODUL 4. MODEL HIDRODINAMIKA 2 DIMENSI
