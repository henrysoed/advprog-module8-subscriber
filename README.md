# Understanding subscriber and message broker

1. What is amqp?

AMQP (Advanced Message Queuing Protocol) adalah sebuah protokol jaringan yang memungkinkan pertukaran data antara sistem yang terpisah. Protokol ini mengatur aturan untuk format, pengiriman, penerimaan, dan interpretasi data. Penggunaan AQMP pada RUST memungkinkan implementasi sistem antar layanan yang efisien, memfasilitasi pengiriman pesan seperti event, request, atau command tanpa keharusan penerima untuk tersedia secara langsung atau terhubung secara langsung dengan pengirim. Hal ini memungkinkan program di platform yang berbeda untuk berkomunikasi dan bertukar data secara efektif.

2. What it means? `guest:guest@localhost:5672` , what is the first guest, and what is the second guest, and what is localhost:5672 is for?

Guest pertama pada `guest:guest@localhost:5672` adalah *username* yang digunakan untuk autentikasi ke server AMQP. Biasanya 'guest' ini merupakan *username default* yang sering digunakan saat menginstal RabbitMQ secara lokal.  Guest kedua pada `guest:guest@localhost:5672`adalah kata sandi yang sesuai dengan username'guest' untuk autentikasi. Sedangkan 'localhost:5672' menunjukkan bahwa server AMQP berjalan di mesin lokal, dan portnya adalah 5672. Dengan demikian, secara keseluruhan, guest:guest@localhost:5672 menginstruksikan aplikasi untuk terhubung ke server AMQP menggunakan nama pengguna 'guest', kata sandi 'guest', melalui port 5672 di mesin lokal.