# Tutorial 8
Nadhira Raihana Hafez
2206082000

* what is amqp?
  AMQP (Advanced Message Queuing Protocol) adalah sebuah protokol yang digunakan untuk mengirim dan menerima pesan di antara aplikasi atau sistem yang berbeda. AMQP memungkinkan aplikasi untuk berkomunikasi secara asinkron, yang berarti pesan dapat ditukar tanpa harus terhubung secara langsung pada saat yang sama atau dalam waktu nyata (real-time).
  

* what it means? guest:guest@localhost:5672 , what is the first guest, and what is
the second guest, and what is localhost:5672 is for?  
`guest:guest@localhost:5672` adalah format address yang menunjukkan username, password, dan lokasi (alamat dan port) dari server yang menggunakan protokol AMQP.
    * `guest` pertama: username atau nama pengguna yang digunakan untuk autentikasi. (nama akun yang digunakan untuk terhubung ke server).  
    * `guest` kedua: password pengguna. Dalam contoh ini, kata sandinya juga "guest".
    * `localhost:5672`: alamat server dan port. "localhost" berarti server berada di lokal. "5672" adalah nomor port (RabbitMQ)