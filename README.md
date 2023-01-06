**JOBSHEET-2-ESP-NOW_CommProtocolSensor**

ESP32 adalah nama dari mikrokontroler yang dirancang oleh perusahaan yang berbasis di Shanghai, China yakni Espressif Systems. ESP32 menawarkan solusi jaringan WiFi dan BLE. ESP32 menggunakan prosesor dual core yang berjalan di instruksi Xtensa LX16. Selain itu, ESP32 telah mendukung protokol komunikasi seperti I2C, UART dan SPI.

**ALAT DAN BAHAN**
1) ESP32
2) Breadboard
3) Kabel jumper
4) Sensor DHT 11, RFID
5) LED (5) dan Push Button (3)
6) Servo
7) Resistor 330,1K, 10K Ohm (@ 3)

**HASIL KELUARAN**

**1. ESP32 Capacitive Touch Sensor**

**Hasil**


**Analisa :** 

Berdasarkan hasil diatas, ESP32 dapat digunakan sebagai Touch Sensor dimana saat kabel jumper disentuh maka akan menghasilkan data pada serial plotter. Kemudian, apabila ketika sensor dari kabel tidak disentuh maka nilai pada serial plotter akan tinggi. Sedangkan, kebalikannya saat sensor disentuh maka serial plotter akan rendah.

**Kemudian Buatlah Rangkaian dibawah ini**
![image]

**Keluaran** 

a) Lampu LED On saat disentuh dan Off saat tidak disentuh

**Analisa :** 
Berdasarkan hasil diatas, implementasi dari nilai serial plotter untuk menghidupkan dan menyalakan lampu LED dapat dilakukan dengan memasukkan perintah if else pada program. Hasil yang diperoleh adalah lampu LED akan menyala ketika sensor disentuh dan sebaliknya lampu LED akan mati ketika sensor tidak disentuh. 

b) Lampu LED akan menyala Blink saat disentuh 

**Analisa :** 
Berdasarkan hasil diatas, implementasi dari nilai serial plotter hanya dapat diatur pada programnya. Sehingga, apabila ketika sensor disentuh maka yang terjadi adalah lampu LED akan menyala BLINK dan sebaliknya akan dalam kondisi mati ketika sensor tidak disentuh.

c) Ketika LED menyala Serial Monitor akan menampilkan angka yang bertambah tiap kali sensor disntuh 

**Analisa :** 
Berdasarkan hasil diatas, menghasilkan sebuah data dimana ketika sensor tersebut disentuh maka akan mengirimkan data untuk menambahkan angka yang akan tampil pada serial monitor.

d) Lampu LED akan menyala Running saat sensor disentuh

**Analisa :** 
Berdasarkan hasil diatas, program akan diubah sehingga apabila ketika sensor disentuh maka yang akan terjadi adalah lampu LED akan menyala secara running dari kiri ke kanan dan kemudian berubah dari kanan ke kiri secara kontinyu.

**2. DHT 11 Sensor** 

Berdasarkan hasil diatas, program tersebut menggunakan sensor suhu dan kelembapan DHT11 yang dapat menghasilkan sebuah data sehingga dapat disimpan pada ESP32. Untuk rangkaiannya seperti ini:

![image](https://user-images.githubusercontent.com/41616849/209120548-e0bac69c-7d9b-4002-87f5-0a7e16526ae0.png)

Rangkaian diatas kemudian akan ditambah dengan buzzer yang akan menyala saat sensor membaca suhu 30 derajat celcius dan 3 buah lampu LED akan menyala secara running saat suhu dibawah 30 derajat celcius.


**Analisa :** 
Berdasarkan hasil diatas, melalui data yang telah diperoleh maka sensor DHT11 dapat membuat program dengan memberikan sebuah state pada keadaan tertentu. 


**3. Sensor RFID**

**Buatlah rangkaian seperti berikut**

![image](https://user-images.githubusercontent.com/41616849/209123901-b261bf28-8be5-443a-aadf-cb393fa20e94.png)


Keluaran 

![image](https://user-images.githubusercontent.com/41616849/209123721-e27870b9-23ab-4e33-afd5-f146bd19903d.png)

**Analisa :** 

Berdasarkan hasil diatas, kondisi yang akan terjadi adalah apabila Tag RFID didekatkan pada sebuah Reader, maka lampu LED Hijau akan menyala, servo akan bergerak ke kanan kemudian kembali ke posisi semula setelah 3 detik dan pada Serial Monitor akan menampilkan pesan “Akses Diterima, Silahkan Masuk”. Selanjutnya, apabila kondisi Tag RFID tidak dikenali, maka yang terjadi adalah lampu LED Merah akan menyala, servo akan menjadi tidak bergerak dan pada Serial Monitor akan menampilkan sebuah pesan “Akses Ditolak”.

Keluaran 

**Analisa :** 

Setelah mengetahui tentang cara kerja RFID pada percobaan diatas maka kita akan dapat menambahkan sebuah motor servo. Ketika kartu akses diterima maka yang akan terjadi pada ESP32 adalah akan mengirimkan sebuah data pada motor servo untuk berputar sebesar 180 derajat selama 3 detik dan akan kembali ke posisi semula kemudian lampu LED hijau akan menyala. Sedangkan, apabila dalam kondisi ketika kartu akses ditolak maka lampu LED merahlah yang akan menyala.
