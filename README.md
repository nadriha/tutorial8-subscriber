# Tutorial 8

* what is amqp?
  AMQP (Advanced Message Queuing Protocol) adalah sebuah protokol yang digunakan untuk mengirim dan menerima pesan di antara aplikasi atau sistem yang berbeda. AMQP memungkinkan aplikasi untuk berkomunikasi secara asinkron, yang berarti pesan dapat ditukar tanpa harus terhubung secara langsung pada saat yang sama atau dalam waktu nyata (real-time).
  

* what it means? guest:guest@localhost:5672 , what is the first guest, and what is
the second guest, and what is localhost:5672 is for?  
`guest:guest@localhost:5672` adalah format address yang menunjukkan username, password, dan lokasi (alamat dan port) dari server yang menggunakan protokol AMQP.
    * `guest` pertama: username atau nama pengguna yang digunakan untuk autentikasi. (nama akun yang digunakan untuk terhubung ke server).  
    * `guest` kedua: password pengguna. Dalam contoh ini, kata sandinya juga "guest".
    * `localhost:5672`: alamat server dan port. "localhost" berarti server berada di lokal. "5672" adalah nomor port (RabbitMQ)

![image](https://github.com/nadriha/tutorial8-subscriber/assets/116888619/b491ec2e-97d0-4c45-b012-610b64372c54)
Pada eksekusi dengan sleep, terlihat bahwa terdapat spike yang menyentuh angka 10 pada grafik queued message di atas. Hal ini terjadi karena ketika menjalankan 3 perintah cargo run dengan cepat pada publisher sehingga terdapat 15 pesan yang dikirim perlu dimasukkan ke queue terlebih dahulu.

![image](https://github.com/nadriha/tutorial8-subscriber/assets/116888619/2638d3c8-bd44-4280-8116-a0d9986dd4e8)
![image](https://github.com/nadriha/tutorial8-subscriber/assets/116888619/be399882-5062-4c3b-8758-8cf61dea1221)

Pada saat saya menjalankan 2 subsctiber sekaligus, semua pesan yang dikirim dibagi eksekusinya ke 2 subscriber tersebut. Hal ini mengakibatkan grafik yang dihasilkan seperti pada gambar kedua. Meskipun dieksekusi dengan sleep, dapat dilihat dari grafik queued messages, sekarang queued message tidak mencapai angka 10, akan tetapi menurun hingga 7.5. Hal ini terjadi karena message telah dieksekusi oleh 2 subscriber berbeda sehingga message tidak perlu lagi mengantri di queue untuk dieksekusi.

