# Menghubungkan Perangkat Raspberry Pi dan Komputer menggunakan Kabel Ethernet STRAIGHT RJ45
Pada catatan ini secara spesifik akan dijelaskan langkah-langkah yang diperlukan untuk menghubungkan perangkat Raspberry Pi langsung pada komputer (PC/Laptop) dengan menggunakan kabel ethernet jenis straight dengan penghubung RJ45. Terdapat 3 cara untuk menghubungkan perangkat Rapsberry Pi dan komputer menggunakan kabel ethernet, diantaranya:
1. Dengan kabel ethernet STRAIGHT RJ45 dengan melalui perangkat router (Raspberry Pi ---> Router ---> Komputer)
2. Dengan kabel ethernet CROSS RJ45 secara langsung (Raspberry Pi ---> Komputer)
3. Dengan kabel ethernet STRAIGHT RJ45 secara langsung (Raspberry Pi ---> Komputer)

Pada catatan ini, akan saya bahas untuk skenario ke-3, yaitu menghubungkan antara perangkat Raspberry dan komputer/laptop secara langsung (tanpa menggunakan perantara router) dengan menggunakan kabel ethernet RJ45 STRAIGHT. Sebelum melanjutkan langkah selanjutnya, pastikan seluruh proses instalasi dan persiapan pada [Instalasi Raspberry Pi](https://github.com/rizalespe/Catatan-Konfigurasi-Instalasi/blob/master/Install_Raspberry_Pi_ID.md) telah selesai dilakukan. 

### Persiapan
1. Buka SD Card pada file exploler (Windows Exploler), kemudian tambahkan file kosong dengan nama 'ssh' tanpa ekstensi apapun seperti '.txt'
2. Pasang SD Card yang telah berisi sistem operasi pada perangkat Raspberry Pi. 
3. Sambungkan sumber listrik dengan kabel data USB pada perangkat Raspberry Pi.
4. Sambungkan perangkat Raspberry Pi dan komputer menggunakan kabel ethernet STRAIGHT RJ45. Pastikan lampu indikator pada kabel ethernet menyala pada kedua sisi.
5. Perangkat lunak untuk remote SSH Putty [Unduh Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html). Kemudian lakukan instalasi Putty.

### Langkah-langkah
1. Buka ```Settings``` > ```Network & Internet``` > ```Network & Sharing Center```. Raspberry Pi terhubung pada ethernet dengan unidentified network seperti pada gambar yang dilingkari di bawah ini. 

![Network Configuration](https://github.com/rizalespe/Catatan-Konfigurasi-Instalasi/blob/master/network-configuration.JPG)

2. Buka command prompt (CMD) dan jalankan perintah ```ipconfig /all``` dan scroll ke bagian atas untuk menemukan ```Ethernet adapter```. 
3. Pada komputer yang saya gunakan, pada ethernet adapter tersebut memiliki IP ```169.254.15.188 (Preferred)```. IP tersebut merupakan alamat Gateway pada ethernet adapter. Kemudian untuk dapat diakses menggunakan laptop kita, perangkat Raspberry Pi akan kita set untuk memiliki IP 169.254.15.X (nilai X dapat kita tentukan sendiri).
4. Putus sumber listrik pada perangkat Raspberry Pi, lepas SD Card yang terpasang, dan buka SD Card pada komputer.
5. Buka file ```cmdline``` pada text editor (Notepad atau yang lainnya)
6. Tanpa menekan tombol Enter, tambahkan pada baris yang sama ```ip=169.254.15.X``` (nilai X dapat diubah dengan angka lain)
7. Simpan file, keluar dari text editor, pasang SD Card pada perangkat Raspberry dan sambungkan perangkat Raspberry dengan sumber listrik
8. Buka aplikasi Putty yang telah terinstall, masukan alamat IP yang telah ditentukan pada proses nomor 6 dengan port 22 dan klik Open
9. Apabila ada pop-up yang muncul terkait dengan PuTTY Security Alert, klik Yes.
10. Secara default, login pada perangkat Raspberry Pi yaitu dengan ```username: pi``` dan ```password: raspberry```
11. Apabila login berhasil, maka akan muncul tampilan berikut ini:

![Login Success](https://github.com/rizalespe/Catatan-Konfigurasi-Instalasi/blob/master/login-raspberry-pi.JPG)


Sekarang, anda telah terhubung dengan perangkat Raspberry Pi tanpa membutuhkan monitor/display, keyboard/mouse, dan menggunakan kabel ethernet RJ45 STRAIGHT. Selesai.
