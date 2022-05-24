# TUGAS-AKHIR-PEMOS

Repositori ini dibuat untuk memenuhi Tugas Akhir Praktikum Pemodelan Oseanografi 2022 oleh Kelompok 1 Oseanografi 2020. Repositori ini memuat materi dan persamaan dari modul 1-4, yaitu Persamaan Adveksi-Difusi 1 Dimensi dan 2 Dimensi, serta Model Hidrodinamika 1 Dimensi dan 2 Dimensi. _Script_ yang dibuat dalam repositori ini menggunakan bahasa _python_ menggunakan _platform Jupyter Notebook_. _Library_ yang digunakan meliputi _numpy, matplotlib_, serta tambahan data gelombang dari _National Buoy Data Center_ (NDBC) melalui _website_ (https://www.ndbc.noaa.gov/obs.shtml). Seluruh _script_ ini merupakan hasil dari kerja Kelompok 1 Oseanografi 2020.
Terima kasih dan semoga bermanfaat!

# ANGGOTA KELOMPOK 1
1. Aloysius Dimas Sanjaya Saliyo          26050120130056 A

2. Fairus Jamil Rizqullah                 26050120140103 B

3. Dafina Amadita Shaquilla               26050120140168 A

4. Vanessa Kurniawan                      26050120140092 B

5. Khana Nadira Sastradjaja               26050120140166 B

6. Bagas Priambodo                        26050120140143 B

7. Priska E. Lumban Batu 26050120120031 A

8. Laurentia Levina Pramestanti           26050120140126 B



# MODUL 1. PERSAMAAN ADVEKSI-DIFUSI 1 DIMENSI 📌
Perubahan temperature di badan air disebabkan oleh proses fisis. Proses fisis tersebut berupa adveksi difusi, konduksi, dan konveksi.Persebaran panas dapat dikaji dengan menggunakan pendekatan pemodelan yang dioperasikan melalui komputer. Difusi adalah proses perpindahan panas berupa rambatan dari air dengan temperatur tinggi ke air dengan temperatur yang lebih rendah. Biasanya permukaan laut lebih panas dari udara di atasnya sehingga terdapat sejumlah panas yang hilang dari laut melalui proses konduksi. Kehilangan tersebut relatif kecil dibanding total panas lautan sehingga pengaruhnya dapat diabaikan, kecuali untuk pencampuran konvektif oleh angin yang memindahkan udara hangat dari permukaan laut. Dengan kata lain luas sebaran polutan panas dari kanal pendingin tergantung pada beberapa faktor yaitu volume air limbah, temperatur air limbah, temperatur ambien air laut dan sirkulasi air laut di lokasi masuknya air limbah ke laut (Cahyana, 2011).
   
•	Jenis-Jenis Difusi
Difusi dibedakan menjadi dua, yaitu difusi biasa dan khusus. Inilah uraiannya:
1)	Difusi Biasa
Sel ingin mengambil nutrisi, atau terjadi pada molekul/partikel hydropobhic (tidak berpolar). Partikel akan langsung berdifusi tanpa memerlukan energi, dan bisa melewati membran langsung.
2)	Difusi Khusus
Terjadi di sel yang ingin mengambil nutrisi, terjadi di partikel yang punya polar/ion (hydrophilic). Diperlukan protein yang khusus agar partikel bisa melewati membran.

•	Faktor Mempengaruhi Difusi
1.	Suhu, makin tinggi difusi makin cepat
2.	BM makin besar difusi makin lambat
3.	Kelarutan dalam medium, makin besar difusi makin cepat
4.	Perbedaan Konsentrasi, makin besar perbedaan konsentrasi antara dua bagian, makin besar proses difusi yang terjadi.
5.	Jarak tempat berlangsungnya difusi, makin dekat jarak tempat terjadinya difusi, makin cepat proses difusi yang terjadi.
6.	Area Tempat berlangsungnya Difusi, makin luas area difusi, makin cepat proses difusi.

•	Proses Difusi
Proses difusi merupakan perpindahan molekul larutan berkonsentrasi tinggi menuju larutan berkonsentrasi rendah tanpa melalui selaput membran. Contoh yang sederhana adalah pemberian gula pada cairan teh tawar. Lambat laun cairan menjadi manis. Contoh lain adalah uap air dari cerek yang berdifusi dalam udara, dimana pada masing-masing zat, kecepatan difusi berbeda-beda.

Proses difusi dalam sistem farmasetik:

𝐽= 𝑑𝑀 𝑆.𝑑𝑡

Keterangan:

J = fluks (g/cm2det)

M = jumlah massa (g atau mol)

S = luas permukaan (cm2)

t = waktu (detik)

•	Hukum Pertama Difusi Fick
Fluks, berbanding lurus dengan gradien konsentrasi, dc/dZ

𝐽 = −𝐷 𝑑𝑐 𝑑𝑧

Keterangan:

D = koefisien difusi (cm2/det)

C = konsentrasi (g/cm3)x = jarak (cm)

Tanda negatif pada persamaan menandakan bahwa difusi terjadi dalam arah yang berlawanan dengan kenaikan konsentrasi (arah x positif).

•	Hukum Kedua Difusi Fick
Konsentrasi difusan dalam elemen volume berubah seiring waktu, yaitu ΔC/Δt, sementara fluks atau jumlah zat yang berdifusi berubah seiring jarak, ΔJ/ΔZ, dalam arah Z, atau
𝑑𝑐 𝑑𝑡 = 𝑑𝐽 𝑑𝑍
𝑑𝑐 𝑑𝑧 = −𝐷 𝑑 𝑑𝑍 𝑑𝑐 𝑑𝑍
𝑑𝑐 𝑑𝑧 = −𝐷 𝑑 2 𝑐 𝑑 𝑍 2

•	Hukum Difusi Fick
Dalam hukum Fick ketika sebuah lapisan tipis dari sebuah diffusant berada bagian ditengah dari sebuah cell silender yang panjang dengan waktu pada jarak Z dari pusat maka

𝐶 𝑍,𝑡 = η 𝑜 2𝜋𝐷𝑡 𝑒 − ( 𝑍 2 4𝐷𝑡 )

Untuk peristiwa difusi, Adolph Fick mengambil analogi yang menyatakan bahwa:

“Pada arah tertentu, massa dari suatu bahan terlarut yang melewati suatu luasan tertentu tiap unit waktu adalah sebanding dengan gradient konsentrasi bahan terlarut pada arah tersebut”

Untuk proses difusi satu dimensi, hukum Fick menyatakan persamaan matematika sebagai berikut: 

q=-D ∂c/∂x

Dengan q adalah fluks massa bahan terlarut, C konsentrasi bahan terlarut, D koefisien difusi, tanda negative merupakan penanda bahwa bahan terlarut terangku dari tempat yang berkonsentrasi tinggi ke tempat yang berkonsentrasi rendah D merupakan koefisien difusi atau difusi molekuler. Hukum Fick merupakan pernyataan yang mengkorelasikan fluks suatu massa dengan gradient konsentrasi. 


Soal

Sebuah larutan berwarna ditempatkan dalam lapisan tipis di tengah sel silinder yang panjang. Jika difusi dibiarkan terus selama 1 jam dua puluh menit, hitunglah konsentrasi larutan warna dalam mol dm-3 pada jarak 1 cm dari posisi asli dari lapisan tipis dengan asumsi bahwa difusi koefisien pewarna adalah 0.79x 10-9 m2 s-1 dan konsentrasi awal zat warna per satuan luas adalah 10 mol m-2.

Jawab:
𝐶 𝑍,𝑡 = η 𝑜 2𝜋𝐷𝑡 𝑒 − ( 𝑍 2 4𝐷𝑡 )
Z = 1 x 10-2 m, t = 4800 s
Sehingga
𝐶 𝑍,𝑡 = 𝑥 3,142 𝑥 0,79 𝑥 10 −9 𝑥 𝑒 − ( −4 4𝑥 0, −9 𝑥 4800 )
= 2,807 mol/m3
= 2,807 x 10-3 mol/dm3
= 0, mol/dm3

Persamaan ini digunakan pada aliran steady yang artinya karakteristik aliran air atau koefisien atau kecepatan alitan dan difusi pada domain tidak berubah terhadap waktu. Koefisien u dan v tidak bernilai konstan tetapi bergantung pada koordinat atau u=u(x,y) dan v=v(x,y). Sedangkan koefisien difusinya bernilai konstan. Pemodelan difusi dapat ditemukan dalam kehidupan sehari-hari seperti pencemaran atau kebakaran hutan. Persamaan difusi dapat dirumuskan sebagai berikut: 
∂F/∂t=A_D  (∂^2 F)/(∂x^2 )

Dekritisasi 1D proses difusi:
F_m^(n+1)=F_m^n+A_D  ∆t/(∆x^2 ) [F_m^(n+1)-2F_m^n+F_(m-1)^n ]

Dekritasi merupakan suatu metode yang digunakan untuk mencari solusi persamaan secara numerik dari suatu persamaan matematika sehingga dapat dikatakan baik dalam dimensi ruang atau pun waktu. 



# MODUL 2. PERSAMAAN ADVEKSI-DIFUSI 2 DIMENSI 📌
**LANGKAH PENGERJAAN:**

`
import matplotlib.pyplot as plt
`

`
import numpy as np
`

`
import sys
`
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

**Perhitungan Energi (U) dan Kecepatan (V) Persebaran Polutan**
```
#Perhitungan U dan V
u = C * np.sin(theta*np.pi/180)
v = C * np.cos(theta*np.pi/180)
dt_count = 1/((abs(u)/(q*dx))+(abs(v)/(q*dy))+(2*ad/(q*dx*2))+(2*ad/(q*dy*2)))
```

**Pembuatan Grafik**

* Menentukan jumlah dan arah persebaran polutan serta banyaknya _time series_
```
Nx = int(x/dx) #number of mesh in x direction
Ny = int(y/dy) #number of mesh in y direction
Nt = int(Tend/dt) #number of timesteps
#Perhitungan Titik Polutan di Buang
px1 = int(px/dx)
py1 = int(py/dy)
```

**Menyederhanakan Fungsi Persamaan Adveksi Difusi 2 Dimensi**
```
lx = u*dt/dx
ly = v*dt/dy
ax = ad*dt/dx**2
ay = ad*dt/dy**2
```

**Memasukkan Syarat Kestabilan CFL**

* Ini dimasukkan untuk menentukan seberapa besar nilai stabilitas dari model yang dibangun
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
  
 **Hasil Pemodelan Output Gambar**
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

Berdasarkan pengolahan data yang dilakukan sebelumnya terlihat bahwasannya persebaran polutan yang ada pada scenario di skema 1, skema 2, skema 3, dan skema 4 hanya memiliki perbedaan pada arah persebarannya saja. Hal ini dikarenakan pada scenario di skema 1, skema 2, skema 3, dan skema 4 memiliki nilai theta yang berbeda-beda. Namun jika dilihat secara seksama, keempat skema tersebut memiliki beberapa karakteristik yang dapat dikatakan sama, dimana pada awal terlihat polutan tersebut sangat pekat berada pada suatu titik hingga lama kelamaan mulai tersebar namun memiliki konsentrasi yang menurun. Hal ini disebabkan persebaran polutan dipengaruhi oleh angin dan arus. Hal ini diperkuat oleh Adriani (2020), dimana angin merupakan faktor pembawa polutan dalam menyebarkan polutan ke tempat lain. Angin tersebut turut ikut berpengaruh terhadap konsentrasi polutan yang ada di perairan.Selain itu, polutan dapat berinteraksi dengan gas lain dari berbagai jenis. Selain itu, terjadinya persebaran polutan dapat disebabkan oleh karena kesetimbangan termal antara suhu polutan dan suhu udara. Berikut saya berikan hasil pengolahan pada saat awal dan akhir pergerakan polutan

**Model ke-1**

![1](https://user-images.githubusercontent.com/106020126/169736983-d2ef66c3-03aa-4513-b07b-bff9187ff835.jpg)

**Model Ke-212**

![212](https://user-images.githubusercontent.com/106020126/169737098-41773676-fd05-44f6-af82-16b94f0d63ce.jpg)



**Pengaplikasian Dari Persamaan Adveksi-Difusi 2 Dimensi**

Dalam memodelkan suatu fenomena gejala alam dapat menggunakan berbagai macam persamaan. Persamaan matematika yang memodelkan fenomena gejala alam adalah persamaan Adveksi-Difusi atau yang sering disebut dengan persamaan transpor. Persamaan Adveksi-Difusi adalah persamaan matematis yang didesain untuk mempelajari fenomena transpor polutan. Triatmojo (1999) menjelaskan bahwa persamaan transpor merupakan salah satu persamaan differensial yang merepresentasikan sirkulasi aliran air di estuari dengan variabel C (Konsentrasi garam) sebagai fungsi ruang dan waktu. Banyak penelitian telah dilakukan tentang penggunaan metode beda hingga dalam menyelesaikan persamaan Adveksi-Diffusi untuk mempelajari fenomena transfer polutan. Kebanyakan penelitian yang telah dilakukan tersebut mempelajari penyebaran polutan pada perairan dengan domain yang teratur dan menggunakan koefisien yang konstan, sedangkan persoalan yang berada disekitar kita menyatakan sebaliknya. Walaupun demikian, metode beda hingga teteap menyediakan solusi numerik yang akurat dan dapat dipakai untuk mendapatkan solusi numerik yang diinginkan (Kusuma, 2014). Dinamika transfer polutan pada perairan ini tentu sangat menarik untuk dikaji, agar kita bisa memprediksi perilaku polutan pada waktu tertentu dan menganalisis akibat dari situasi yang berbeda terhadap perilaku tersebut (Hutomo, et al., 2019).
   
Menurut Alman, (2020). Persamaan matematika yang memodelkan fenomena gejala alam adalah persamaan Adveksi-Difusi atau yang sering disebut dengan persamaan transpor. Fenomena aliran dan transport polutan merupakan gejala alam yang penting untuk dipelajari karena mempunyai pengaruh terhadap beberapa studi rekayasa. Metode beda hingga merupakan salah satu metode yang dapat diterapkan untuk kasus fenomena transport di perairan dangkal dan aliran air tanah yang biasanya dinyatakan dengan persamaan Adveksi -Diffusi 2D karena metode ini dapat memberikan hasil pendekatan yang cukup akurat (Ribal, 2008). Metode beda hingga yang dimodifikasi (digeneralisasikan) ini telah diterapkan di banyak bidang, seperti dalam menganalisis elemen lapisan yang cocok, memecahkan masalah retak bidang, menganalisis pertumbuhan dendritik, kemudian ada pula simulasi numerik pada bidang oseanografi seperi digunakan untuk interaksi gelombang-arus. Metode numerik adalah teknik dasar dimana permasalahan matematika diformulasikan sehingga dapat diselesaikan dengan operasi aritmatika dan logika. Metode numerik ini juga yang mendasari kemudian munculnya persamaan matemati untuk menyelesaikan suatu fenomena alam seperti persebaran polutan. Perkembangan komputer dengan waktu komputasi yang semakin cepat, membuat pemodelan matematika semakin banyak diminati, dengan penerapan metodemetode numerik yang mempermudah dalam menyelesaikan persamaan-persamaan matematis pada model matematika yang telah dibuat. Karena komputer digital unggul dalam melakukan operasi semacam itu, metode numerik kadang disebut sebagai matematika komputer.


# MODUL 3. MODEL HIDRODINAMIKA 1 DIMENSI 📌
Pada contoh script Pemodelan Hidrodinamika 1D ini merupakan penyelesaian hitungan guna mengetahui bagaimana hubungan elevasi muka air laut dan juga kecepatan arus terhadap ruang dan waktu. Pada script ini menggunakan bahasa pemrograman pyhton dan menggunakan library Matplotlib yang berguna menampilkan visualisasi hasil code dan juga library Numpy untuk perhitungan scientific

**Langkah Pengerjaan**

```
import matplotlib.pyplot as plt
import numpy as np
``` 
**Penginputan Nilai Parameter**

```
#Proses Awal
p = 5000         
T = 1200         
A = 0.5         
D = 15           
dt = 2
dx = 100
To = 300         

#Parameter Lanjutan
g = 9.8   
pi = np.pi 
C = np.sqrt(g*D) 
s = 2*pi/To      
L = C*To         
k = 2*pi/L       
Mmax = int(p//dx)
Nmax = int(T//dt)`
``` 
***Penyelesaian Persamaan Hidrodinamika***
```
zo = [None for _ in range(Mmax)]
uo = [None for _ in range(Mmax)]

hasilu = [None for _ in range(Nmax)]
hasilz = [None for _ in range(Nmax)]
```
***Penggunaan perintah looping untuk penyelesaian range untuk nilai uo dan zo***
```
for i in range(1, Mmax+1):
  zo[i-1] = A*np.cos(k*(i)*dx)
  uo[i-1] = A*C*np.cos(k*((i)*dx+(0.5)*dx))/(D+zo[i-1])
for i in range(1, Nmax+1):
  zb = [None for _ in range(Mmax)]
  ub = [None for _ in range(Mmax)]
  zb[0] = A*np.cos(s*(i)*dt)
  ub[-1] = A*C*np.cos(k*L-s*(i)*dt)/(D+zo[-1])
  for j in range (1, Mmax):
    ub[j-1] = uo[j-1]-g*(dt/dx)*(zo[j]-zo[j-1])
  for k in range(2, Mmax+1):
    zb[k-1] = zo[k-1]-(D+zo[k-1])*(dt/dx)*(ub[k-1]-ub[k-2])
    hasilu[i-1] = ub
    hasilz[i-1] = zb
  for p in range(0, Mmax):
    uo[p] = ub[p]
    zo[p] = zb[p]
```

***Pembuatan Grafik***
```
def rand_col_hex_string():
  return f'#{format(np.random.randint(0,16777215), "#08x")[2:]}

hasilu_np = np.array(hasilu)
hasilz_np = np.array(hasilz)

fig0, ax0 = plt.subplots(figsize=(12,8))
for i in range (1, 16):
  col0 = rand_col_hex_string()
  line, = ax0.plot(hasilu_np[:,i-1], c=col0, label=f'n={i}')
  ax0.legend()

  ax0.set(xlabel='Waktu', ylabel='Kecepatan Arus', title='''Shafina Amalia Yahya_26050120140169
  Perubahan Kecepatan Arus Dalam Grid Tertentu di sepanjang Waktu''')
  ax0.grid()

fig1, ax1 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
  col1= rand_col_hex_string()
  line, = ax1.plot(hasilz_np[:,i-1], c=col1, label=f'n={i}')
  ax1.legend()

  ax1.set(xlabel='Waktu', ylabel='Elevasi Muka Air', 
          title='''Shafina Amalia Yahya_26050120140169
          Perubahan Elevasi Permukaan Air Dalam Grid Tertentu di sepanjang Waktu''')
  ax1.grid()

fig2, ax2 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
  col2= rand_col_hex_string()
  line, = ax2.plot(hasilu_np[i-1], c=col2, label=f't={i}')
  ax2.legend()

  ax2.set(xlabel='Grid', ylabel='Kecepatan Arus', 
          title='''Shafina Amalia Yahya_26050120140169
          Perubahan Kecepatan Arus Dalam Waktu Tertentu di Sepanjang Grid''')
  ax2.grid()

fig3, ax3 = plt.subplots(figsize=(12,8))
for i in range(1, 16):
  col3= rand_col_hex_string()
  line, = ax3.plot(hasilz_np[i-1], c=col3, label=f't={i}')
  ax3.legend()

  ax3.set(xlabel='Grid', ylabel='Elevasi Muka Air', 
          title='''Shafina Amalia Yahya_26050120140169
          Perubahan Elevasi Muka Air Dalam Waktu Tertentu di Sepanjang Grid''')
  ax3.grid()
```
Perintah untuk menampilkan hasil grafik pemodelan Hidrodinamika 1D

`plt.show()`




**PEMBAHASAN:**

**HASIL RUNNING SCRIPT PEMODELAN HIDRODINAMIKA 1 DIMENSI**

**a. Perubahan Kecepatan Arus dalam Grid Tertentu di Sepanjang Waktu**

![1](https://user-images.githubusercontent.com/105528467/170018403-71369062-1ae6-43b3-bd81-bbdcf18d20b7.png)

Hasil model hidrodinamika 1 D pada grafik menunjukkan perubahan kecepatan arus dalam grid (n=1 sampai n=15) dalam kurun waktu 0 sekon sampai 175 sekon. Pada grafik, garis awalnya grafiknya halus dan teratur serta sederhana. Perubahan kecepatan dalam grid atau garis yang halus dan teratur tersebut menunjukkan nilai perubahan kecepatan arus berkisar -0,5 meter sampai 0,5 meter. Hal tersebut dikarenakan perhitungannya masih menggunakan parameter yang ada dicoding bagian awal yang nilainya kecil. Akan tetapi, seiring berjalannya waktu ke arah sumbu-x dalam kurun waktu sekitar 176 sekon sampai 600 sekon ditampilkan perubahan kecepatan arus dalam grid atau garis yang semakin kasar dan tidak teratur serta rumit yang nilai kecepatan arusnya berkisar antara -1,5 meter sampai 1,5 meter. Hal ini disebabkan oleh nilai dari setiap parameter-parameter yang digunakan semakin besar dan perhitungannya semakin kompleks dan rumit. Walaupun demikian, nilai yang rumit dan kompleks tersebut menunjukkan bahwa perhitungan benar dan hasil perhitungan semakin mendekati keadaan sebenarnya ditempat terjadinya perubahan kecepatan arus tersebut.

**b. Perubahan Elevasi Permukaan Air dalam Grid Tertentu di Sepanjang Waktu**

![2](https://user-images.githubusercontent.com/105528467/170019555-b1eefb88-fab9-4832-aaaf-792da59a6a1b.png)

Hasil model hidrodinamika 1 D pada grafik ini sebenarnya hampir sama dengan sebelumnya dimana grafik ini menunjukkan perubahan elevasi muka air dalam grid (n=1 sampai dengan n=15) dalam waktu kurun waktu 0 sekon sampai sekitar 175 sekon ditampilkan pada garis awal grafiknya halus dan teratur serta sederhana dimana dalam grafik ini, perubahan elevasi muka air dalam grid atau garis yang halus tersebut menunjukkan nilai perubahan elevasi muka air berkisar -0,5 meter sampai 5 meter. Hal tersebut dikarenakan perhitungannya masih menggunakan parameter yang ada di coding bagian awal yang nilainya kecil. Akan tetapi, seiring berjalannya waktu ke arah sumbu-x dalam kurun waktu sekitar 176 sekon sampai 600 sekon ditampilkan perubahan elevasi muka air dalam grid atau garis yang semakin kasar dan tidak teratur serta rumit yang nilai kecepatan arusnya berkisar antara -2 meter samapi 2 meter. Hal ini dikarenakan nilai dari setiap parameter-parameter yang digunakan semakin besar dan perhitungannya semakin kompleks. Walaupun demikian, nilai yang rumit dan kompleks tersebut menunjukkan bahwa perhitungan benar dan hasil perhitungan semakin mendekati keadaan sebenarnya ditempat terjadinya perubahan kecepatan arus. 

**c. Perubahan Kecepatan Arus dalam Waktu Tertentu di Sepanjang Grid**

![3](https://user-images.githubusercontent.com/105528467/170019607-7217ee12-e0e3-487a-9cd0-1bbd6b4fa933.png)

Hasil model hidrodinamika 1 D pada grafik menunjukkan bahwa garis grafik di awal halus dan semakin lama ke arah sumbu-x semakin tidar teratur. Pada grafik ditampilkan pada grid sekitar 0 - 43 dengan kisaran waktu t=1 sampai dengan t=15 memiliki nilai kecepatan arus dalam grid berkisar -0.4 meter sampai 0.4 m. Sedangkan pada grid sekitar 44 – 50 dengan waktu yang sama dengan grid 0 - 43 memiliki kecepatan arus berkisar antara -0,2 meter sampai 0,4 meter.  Hal tersebut disebabkan terjadinya perubahan kecepatan arus terjadi dalam satu waktu atau waktu yang sama tetapi dalam ruang /grid yang berbeda sehingga mempengaruhi nilai dari parameter-parameter perhitungan. Grid paling depan menerima konsekuensi arus dan elevasi lebih dahulu disusul dengan grid-grid lainnya. 

**d. Perubahan Elevasi Permukaan Air dalam Waktu Tertentu di Sepanjang Grid**

![4](https://user-images.githubusercontent.com/105528467/170019636-b3f6feba-1834-4cc9-8a26-1d428e0bf12b.png)

Hasil model hidrodinamika 1 D pada grafik menunjukkan bahwa garis grafik di awal halus dan semakin lama ke arah sumbu-x semakin tidar teratur. Pada grafik ditampilkan pada grid sekitar 0 - 43 dengan kisaran waktu t=1 sampai dengan t=15 memiliki nilai elevasi muka air dalam grid berkisar -0.7 meter sampai 0.5 m. Sedangkan pada grid sekitar 44 – 50 dengan waktu yang sama dengan grid 0 - 43 memiliki kecepatan arus berkisar antara 0,0 meter sampai -0,7 meter.  Hal tersebut disebabkan terjadinya perubahan kecepatan arus terjadi dalam satu waktu atau waktu yang sama tetapi dalam ruang /grid yang berbeda sehingga mempengaruhi nilai dari parameter-parameter perhitungan. Variasi nilai kecepatan arus dan elevasi muka air adalah sama di setiap grid setiap waktu.


# MODUL 4. MODEL HIDRODINAMIKA 2 DIMENSI 📌
"LANGKAH PENGERJAAN"

```
import matplotlib.pyplot as plt
from siphon.simplewebservice.ndbc import NDBC
```
```
# Get a pandas data frame of all of the observations, meteorological data is the default
# observation set to query.
df = NDBC.realtime_observations('46015') #Station ID
df.head()
```
```
# let's make a simple time series plot to checkout what the data look like.
fig, (ax1, ax2, ax3) = plt.subplots(3, 1, figsize=(12,10))
ax2b = ax2.twinx()
```

**Membuat Grafik Tekanan Udara**
```
#Pressure
ax1.plot(df['time'], df['pressure'], color='black')
ax1.set_ylabel('Pressure [hPa]')
fig.suptitle('nama_nim', fontsize=18)
```

**Membuat Gafik Kecepatan, hembusan dan arah angin**
```
#Wind speed, gust, direction
ax2.plot(df['time'], df['wind_speed'], color='tab:orange')
ax2.plot(df['time'], df['wind_gust'], color='tab:olive', linestyle='--')
ax2b.plot(df['time'], df['wind_direction'], color='tab:blue', linestyle='-')
ax2.set_ylabel('Wind Speed [m/s]')
ax2b.set_ylabel('Wind Direction')
```

**Membuat Grafik Temperatur Air**
```
#Water temperature
ax3.plot(df['time'], df['water_temperature'], color='tab:brown')
ax3.set_ylabel('Water Temperature [degC]')
```
```
plt.show()
```

**PEMBAHASAN:**
```
Studi Kasus: Stasiun Buoy 41009
```
**Lokasi Stasiun Buoy 41109**

![lokasi](https://user-images.githubusercontent.com/106019440/170066521-e56038b6-9cf7-4584-b04e-6335c6cdfea9.png)
**Stasiun Buoy 41109**

![buoy](https://user-images.githubusercontent.com/106019440/170065954-5928a3a4-863e-4477-888c-ba26d3a41451.jpg)

Stasiun buoy 41009 terletak pada koordinat 28.508 N 80.185 W (28°30'27" N 80°11'6" W). Berdasarkan koordinat tersebut, jika dilihat menggunakan software Google Earth Pro, stasiun buoy 41009 berada sejauh kurang lebih 35,88 km di timur Brevard County, Florida, Amerika Serikat. Stasiun tersebut berada pada perairan Samudera Atlantik yang masih terbilang cukup dekat dengan pantai dengan kedalaman 42 m. Hal tersebut menyebabkan stasiun buoy 41009 mendapatkan pengaruh yang cukup kuat dari Samudera Atlantik. Samudra Atlantik merupakan wilayah luas yang merupakan tempat terjadinya bemacam-macam fenomena hidro-oseanografi, bahkan meteo-oseanografi. Salah satunya adalah terbentuknya badai/siklon tropis yang disebut juga dengan Hurricane karena terbentuk di Samudra Atlantik. Menurut Dyahwati et al. (2007), siklon tropis merupakan suatu peristiwa rendahnya tekanan atmosfer yang disertai dengan tingginya suhu permukaan laut dan kecepatan angin. Berdasarkan hasil model, dapat dilihat bahwa terjadi pola anomali di wilayah perairan di mana stasiun buoy 41009 berada, yakni di perairan Samudra Atlantik. Pada time series 2022-04-08, tekanan atmosfer terbilang rendah, namun kecepatan angin dan suhu air laut terbilang cukup tinggi. Hal tersebut menciptakan suatu anomali yang kemudian mengindikasikan terjadinya atau terbentuknya siklon tropis atau badai tropis. Hal yang sama juga terjadi pada time series 2022-05-01, namun anomali yang terjadi tidak sebesar pada time series 2022-04-08.

**Hasil Model Perubahan Suhu Air Laut, Kecepatan Angin, dan Tekanan Atmosfer terhadap Waktu**
![hasil model](https://user-images.githubusercontent.com/106019440/170068020-0afbd934-9a90-4557-92b8-ffa41b0b70f8.png)


## **UCAPAN TERIMA KASIH**
Demikian _repository_ Tugas Akhir Praktikum Pemodelan Oseanografi 2022. Apabila ada kesalahan dalam penulisan kami memohon maaf. Kami juga berterima kasih kepada Kakak-Kakak Asisten yang telah mendampingi dan membimbing serta teman-teman oseanografi 2020 yang telah bekerja keras selama berjalannya Praktikum Pemodelan Oseanografi. 
