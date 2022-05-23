# TUGAS-AKHIR-PEMOS

Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi 2022 oleh Kelompok 1 Oseanografi 2020. Repositori ini memuat materi dan persamaan dari modul 1-4, yaitu Persamaan Adveksi-Difusi 1 Dimensi dan 2 Dimensi, serta Model Hidrodinamika 1 Dimensi dan 2 Dimensi. _Script_ yang dibuat dalam repositori ini menggunakan bahasa _python_ menggunakan _platform Jupyter Notebook_. _Library_ yang digunakan meliputi _numpy, matplotlib_, serta tambahan data gelombang dari _National Buoy Data Center_ (NDBC) melalui _website_ (https://www.ndbc.noaa.gov/obs.shtml). Seluruh _script_ ini merupakan hasil dari kerja Kelompok 1 Oseanografi 2020.
Terima kasih dan semoga bermanfaat!

# ANGGOTA KELOMPOK 1
1. Aloysius Dimas Sanjaya Saliyo          26050120130056 A

2. Fairus Jamil Rizqullah

3. Dafina Amadita Shaquilla               26050120140168 A

4. Vanessa Kurniawan

5. Khana Nadira Sastradjaja               26050120140166 B

6. Bagas Priambodo

7. Priska E. Lumban Batu

8. Laurentia Levina Pramestanti           26050120140126 B



# MODUL 1. PERSAMAAN ADVEKSI-DIFUSI 1 DIMENSI 📌




# MODUL 2. PERSAMAAN ADVEKSI-DIFUSI 2 DIMENSI 📌
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

**Menyederhanakan Fungsi**
```
lx = u*dt/dx
ly = v*dt/dy
ax = ad*dt/dx**2
ay = ad*dt/dy**2
```

**Memasukkan Syarat Kestabilan CFL**
Ini dimasukkan untuk menentukan seberapa besar nilai stabilitas dari model yang dibangun
```
cfl = (2*ax + 2*ay + abs(lx) + abs(ly)) #Syarat Kestabilan CFL
```

**Pembuatan Grid**
```
x_grid = np.linspace(0-dx, x+dx, Nx+2) #Ghostnode pada boundary
y_grid = np.linspace(0-dx, y+dy, Ny+2) #Ghostnode pada boundary
t = np.linspace(0, Tend, Nt+1)
x_mesh,y_mesh = np.meshgrid(x_grid,y_grid)
F = np.zeros((Nt+1, Ny+2, Nx+2))
#Kondisi Awal(Initial Condition)
F[0,py1,px1] = Ic
#%%
```

**Memasukkan Iterasi dan Diskritisasi dari Persamaan Adveksi-Difusi 2 Dimensi**
```
#Iterasi
for n in range (0, Nt):
 for i in range (1,Ny+1):
 for j in range(1,Nx+1):
 F[n+1,i,j]=((F[n,i,j]*(1-abs(lx)-abs(ly))) + \
 (0.5*(F[n,i-1,j]*(ly+abs(ly)))) + \
 (0.5*(F[n,i+1,j]*(abs(ly)-ly))) + \
 (0.5*(F[n,i,j-1]*(lx+abs(lx)))) + \
 (0.5*(F[n,i,j+1]*(abs(lx)-lx))) + \
 (ay*(F[n,i+1,j]-2*(F[n,i,j])+F[n,i-1,j])) + \
 (ax*(F[n,i,j+1]-2*(F[n,i,j])+F[n,i,j-1]))) #Diskritisasi
 ```
 
 **Memasukkan Syarat Batas Dari Pembuatan Grafik**
 ```
 #Syarat Batas (Dirichlet Boundary Condition)
 F[n+1,0,:] = 0 #BC Bawah
 F[n+1,:,0] = 0 #BC Kiri
 F[n+1,Ny+1,:] = 0 #BC Atas
 F[n+1,:,Nx+1] = 0 #BC Kanan
  ```
  
 **Hasil Pemodelan**
  ```
  #Output Gambar
 plt.clf()
 plt.pcolor(x_mesh, y_mesh, F[n+1,:,:],cmap = 'jet',shading ='auto',edgecolors = 'k')
 cbar = plt.colorbar(orientation = 'vertical', shrink = 0.95, extend = 'both')
 cbar.set_label(label='Concentration', size = 8)
 #plt.clim(0,100)
 plt.title('Dafina Amadita Shaquilla_26050120140168 \n t='+str(round(dt*(n+1),3))+', Initial
Condition='+str(Ic),fontsize=10)
 plt.xlabel('x_grid',fontsize=9)
 plt.ylabel('y_grid',fontsize=9)
 plt.axis([0, x, 0, y])
 #plt.pause(0.01)
 plt.savefig(str(n+1)+'.jpg', dpi = 300)
 plt.pause(0.01)
 plt.close()
 print('running timestep ke:' +str(n+1) + ' dari:' +str(Nt) + '('+ percentage(n+1,Nt)+')')
 #print('Nilai CFL:' +str(cfl) + ' dengan arah:' +str(theta))
  ```
  
**Hasil Grafik Adveksi-Difusi 2 Dimensi**

Scenario I (θ = 86)

Scenario II (θ = 146)

Scenario III (θ = 221)

Scenario IV (θ = 401)




**PEMBAHASAN:**

**Analisis Hasil Grafik Yang Didapat**

Berdasarkan pengolahan data yang dilakukan sebelumnya terlihat bahwasannya persebaran polutan yang ada pada scenario di skema 1, skema 2, skema 3, dan skema 4 hanya memiliki perbedaan pada arah persebarannya saja. Hal ini dikarenakan pada scenario di skema 1, skema 2, skema 3, dan skema 4 memiliki nilai theta yang berbeda-beda. Namun jika dilihat secara seksama, keempat skema tersebut memiliki beberapa karakteristik yang dapat dikatakan sama, dimana pada awal terlihat polutan tersebut sangat pekat berada pada suatu titik hingga lama kelamaan mulai tersebar namun memiliki konsentrasi yang menurun. Hal ini disebabkan persebaran polutan dipengaruhi oleh angin dan arus. Hal ini diperkuat oleh Adriani (2020), dimana angin merupakan faktor pembawa polutan dalam menyebarkan polutan ke tempat lain. Angin tersebut turut ikut berpengaruh terhadap konsentrasi polutan yang ada di perairan.

**Pengaplikasian Dari Persamaan Adveksi-Difusi 2 Dimensi**

Dalam memodelkan suatu fenomena gejala alam dapat menggunakan berbagai macam persamaan. Persamaan matematika yang memodelkan fenomena gejala alam adalah persamaan Adveksi-Difusi atau yang sering disebut dengan persamaan transpor. Persamaan Adveksi-Difusi adalah persamaan matematis yang didesain untuk mempelajari fenomena transpor polutan. Triatmojo (1999) menjelaskan bahwa persamaan transpor merupakan salah satu persamaan differensial yang merepresentasikan sirkulasi aliran air di estuari dengan variabel C (Konsentrasi garam) sebagai fungsi ruang dan waktu. Banyak penelitian telah dilakukan tentang penggunaan metode beda hingga dalam menyelesaikan persamaan Adveksi-Diffusi untuk mempelajari fenomena transfer polutan. Kebanyakan penelitian yang telah dilakukan tersebut mempelajari penyebaran polutan pada perairan dengan domain yang teratur dan menggunakan koefisien yang konstan, sedangkan persoalan yang berada disekitar kita menyatakan sebaliknya. Walaupun demikian, metode beda hingga teteap menyediakan solusi numerik yang akurat dan dapat dipakai untuk mendapatkan solusi numerik yang diinginkan (Kusuma, 2014). Dinamika transfer polutan pada perairan ini tentu sangat menarik untuk dikaji, agar kita bisa memprediksi perilaku polutan pada waktu tertentu dan menganalisis akibat dari situasi yang berbeda terhadap perilaku tersebut (Hutomo, et al., 2019).
   
Menurut Alman, (2020). Persamaan matematika yang memodelkan fenomena gejala alam adalah persamaan Adveksi-Difusi atau yang sering disebut dengan persamaan transpor. Fenomena aliran dan transport polutan merupakan gejala alam yang penting untuk dipelajari karena mempunyai pengaruh terhadap beberapa studi rekayasa. Metode beda hingga merupakan salah satu metode yang dapat diterapkan untuk kasus fenomena transport di perairan dangkal dan aliran air tanah yang biasanya dinyatakan dengan persamaan Adveksi -Diffusi 2D karena metode ini dapat memberikan hasil pendekatan yang cukup akurat (Ribal, 2008). Metode beda hingga yang dimodifikasi (digeneralisasikan) ini telah diterapkan di banyak bidang, seperti dalam menganalisis elemen lapisan yang cocok, memecahkan masalah retak bidang, menganalisis pertumbuhan dendritik, kemudian ada pula simulasi numerik pada bidang oseanografi seperi digunakan untuk interaksi gelombang-arus. Metode numerik adalah teknik dasar dimana permasalahan matematika diformulasikan sehingga dapat diselesaikan dengan operasi aritmatika dan logika. Metode numerik ini juga yang mendasari kemudian munculnya persamaan matemati untuk menyelesaikan suatu fenomena alam seperti persebaran polutan. Perkembangan komputer dengan waktu komputasi yang semakin cepat, membuat pemodelan matematika semakin banyak diminati, dengan penerapan metodemetode numerik yang mempermudah dalam menyelesaikan persamaan-persamaan matematis pada model matematika yang telah dibuat. Karena komputer digital unggul dalam melakukan operasi semacam itu, metode numerik kadang disebut sebagai matematika komputer.


# MODUL 3. MODEL HIDRODINAMIKA 1 DIMENSI 📌

# MODUL 4. MODEL HIDRODINAMIKA 2 DIMENSI 📌
 
