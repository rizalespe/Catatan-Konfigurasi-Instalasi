# Install Raspberry Pi 3
Catatan ini dibuat untuk memberikan panduan dalam melakukan instalasi sistem operasi pada perangkat Raspberry Pi untuk siap digunakan.

### Persiapan sebelum instalasi
1. Perangkat Raspberry Pi (dalam catatan ini saya menggunakan Raspberry Pi 3)
2. SD Card
3. Kabel data USB
4. Kabel ethernet STRAIGHT RJ45
5. PC/Laptop (dalam catatan ini saya menggunakan sistem operasi MS Windows 10)
6. Image sistem operasi yang dapat diunduh di [unduh image](https://www.raspberrypi.org/downloads/) (dalam catatan ini saya menggunakan [Raspbian](https://www.raspberrypi.org/downloads/raspbian/)). Setelah terunduh, ekstrak file .zip yang di dalamnya terdapat file berekstensi .img.
7. SD Card Formatter yang dapat diunduh di [unduh SD Card Formatter](https://www.sdcard.org/downloads/formatter/). Kemudian lakukan instalasi untuk SD Card Formatter.
8. Balena Etcher yang dapat diunduh di [unduh Balena Etcher](https://www.balena.io/etcher/). Kemudian lakukan instalasi untuk Balena Etcher.

### Format SD Card
Perangkat Rapsberry tidak memiliki media penyimpanan / _storage_ sehingga kita membutuhkan media eksternal sebagai media penyimpanan, dalam hal ini kita menggunakan SD Card. Sebelum SD Card kita gunakan sebagai media penyimpanan dalam Raspberry Pi, yang perlu kita lakukan adalah memastikan bahwa SD Card telah kosong dan tidak berisi data atau sistem operasi lain. Dalam catatan ini saya menggunakan [SD Card Formatter](https://www.sdcard.org/downloads/formatter/) seperti pada tampilan di bawah ini. Untuk melakukan format, pastikan bahwa _select card_ telah menunjuk pada SD Card yang akan kita format, dan klik format.   

![SD Card Formatter](https://github.com/rizalespe/Catatan-Konfigurasi-Instalasi/blob/master/sdcard-formatter.JPG)

### Flashing sistem operasi menggunakan Balena Etcher pada SD Card
Setelah kita pastikan bahwa SD Card telah terformat dengan benar, selanjutnya adalah melakukan _flashing_ sistem operasi yang telah terunduh ke dalam SD Card. Istilah _flashing_ mungkin secara sederhana dapat memiliki makna instalasi. Karena kita tidak dapat hanya melakukan copy-paste secara langsung file image sistem operasi, maka kita gunakan Balena Etcher. Berikut adalah tampilan dari Balena Etcher, yang perlu dipastikan adalah pada bagian kiri telah menunjuk file Raspbian dengan ekstensi .img, bagian tengah telah menunjuk pada media SD Card yang tepat, dan klik Flash untuk memulai proses _flashing_. Proses akan berlangsung beberapa saat, tunggu hingga selesai.

![Balena Etcher](https://github.com/rizalespe/Catatan-Konfigurasi-Instalasi/blob/master/etcher.JPG)

### Pemasangan perangkat
Setelah proses _flashing_ SD Card dengan sistem operasi Raspbian, pasang SD Card pada bagian bawah perangkat Raspberry PI. Tancapkan kabel data USB pada sumber listrik untuk memastikan bahwa perangkat Raspberry Pi mendapatkan power (pastikan lampu LED indikator menyala berwarna merah). Kemudian terakhir, tancapkan kabel ethernet dengan connector RJ45 straight pada kedua sisi perangkat yaitu Raspberry Pi dan laptop/pc yang digunakan. Selesai.

### Selanjutnya...
Setelah persiapan dan instalasi selesai, bagian selanjutnya adalah proses memastikan bahwa secara perangkat lunak telah berjalan pada link berikut:  [Menghubungkan Raspberry Pi menggunakan kabel ethernet STRAIGHT RJ45](). 


