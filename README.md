# JS9-Socket_Programming-Muhamad-Fathur-Rahman

2. Konsep Dasar Socket Programming
2.1 Socket dan Soket Programming

Socket adalah endpoint dalam sebuah saluran komunikasi yang memungkinkan dua program berjalan pada mesin yang berbeda untuk saling bertukar data. Soket programming merupakan pendekatan untuk mengimplementasikan komunikasi antara dua program menggunakan soket.
2.2 Protokol TCP dan UDP

Dalam socket programming, komunikasi dapat menggunakan protokol TCP (Transmission Control Protocol) atau UDP (User Datagram Protocol). Protokol TCP menyediakan koneksi yang dapat diandalkan dan berorientasi koneksi, sementara protokol UDP bersifat lebih sederhana dan tidak berorientasi koneksi.
2.3 Diagram State untuk Model Server dan Client

Perhatikan diagram berikut untuk memahami bagaimana socket bekerja:

Penjelasan diagram:

    Node dibagi menjadi dua jenis: node server dan node klien.
    Node klien mengirimkan sinyal koneksi, dan node server menerima sinyal koneksi dari node klien.
    Koneksi antara node server dan klien dibangun menggunakan soket di lapisan transport internet.
    Setelah koneksi terbentuk, node klien dan server dapat berbagi informasi menggunakan perintah baca dan tulis.
    Setelah pertukaran informasi selesai, node menutup koneksi.

3. WebSocket: Protokol Komunikasi Real-Time
3.1 Pengenalan dan Standarisasi

WebSocket adalah protokol komunikasi komputer yang menyediakan saluran komunikasi dua arah secara simultan melalui satu koneksi Transmission Control Protocol (TCP). Protokol WebSocket telah distandardisasi oleh IETF (Internet Engineering Task Force) sebagai RFC 6455 pada tahun 2011.

Informasi lengkap tentang standar ini dapat dibaca melalui link berikut: RFC 6455.
3.2 Perbedaan dengan HTTP

WebSocket berbeda dengan Hypertext Transfer Protocol (HTTP) yang umumnya digunakan untuk melayani halaman web. Keduanya berada pada lapisan 7 dalam model OSI dan bergantung pada TCP pada lapisan 4.

Meskipun berbeda, WebSocket dirancang untuk berfungsi melalui port HTTP 443 dan 80 serta mendukung proksi dan perantara HTTP, sehingga membuatnya kompatibel dengan HTTP. WebSocket menggunakan HTTP upgrade header untuk beralih dari protokol HTTP ke protokol WebSocket.
3.3 Keuntungan WebSocket

WebSocket memiliki beberapa keuntungan, antara lain:

    Komunikasi dua arah secara langsung dan real-time antara klien dan server.
    Bersifat stateful, tidak seperti protokol HTTP yang bersifat stateless.
    Mengurangi overhead yang terkait dengan membuka dan menutup koneksi yang sering terjadi dalam protokol HTTP.
    Dapat mendukung koneksi cross-domain (dalam konteks keamanan).

4. Socket.IO: Library untuk Socket Programming di Node.js
4.1 Pengenalan Socket.IO

Socket.IO adalah library JavaScript untuk aplikasi web real-time. Library ini memungkinkan komunikasi real-time, dua arah, dan event-based antara klien dan server. Socket.IO menggunakan WebSocket sebagai salah satu transportnya, tetapi dapat dengan otomatis beralih ke transport lain jika WebSocket tidak tersedia.
4.2 Engine.IO dan Socket.IO Protocol

Socket.IO memanfaatkan Engine.IO, yang merupakan transport layer (lapisan transportasi) yang dapat diandalkan dan real-time. Engine.IO memilih transport terbaik yang tersedia, termasuk WebSocket, polling HTTP, dan lainnya.

Socket.IO Protocol adalah protokol khusus yang digunakan oleh Socket.IO untuk pertukaran data antara klien dan server.
4.3 Fitur-fitur Socket.IO

Socket.IO menyediakan berbagai fitur, termasuk:

    Broadcasting: Server dapat memancarkan data ke banyak klien atau ke klien tertentu.
    Room: Klien dapat bergabung dengan "room" tertentu dan menerima pesan hanya dari klien di room tersebut.
    Namespace: Memungkinkan adanya multiple namespaces di satu aplikasi, yang dapat memiliki konfigurasi dan perilaku yang berbeda.

5. Menjalankan Aplikasi dan Investigasi
5.1 Menjalankan Aplikasi

    Buka terminal atau command prompt.
    Arahkan ke folder proyek menggunakan perintah cd path/to/project.
    Install dependencies dengan perintah npm install.
    Jalankan aplikasi dengan perintah node index.js.
    Buka browser dan akses http://localhost:3000.

5.2 Investigasi Console Browser

Buka konsol browser untuk melihat pesan log dan interaksi JavaScript. Gunakan fitur pengembangan (developer tools) pada browser untuk membuka konsol.
6. Pertanyaan dan Tugas
6.1 Pertanyaan Teoritis

    Jelaskan perbedaan antara protokol TCP dan UDP.
    Apa keuntungan penggunaan WebSocket dibandingkan dengan HTTP dalam konteks komunikasi real-time?
    Bagaimana Socket.IO menggunakan Engine.IO dalam implementasinya?
    Jelaskan fungsi dari namespace dalam Socket.IO.

6.2 Investigasi Console Browser

Buka aplikasi chat yang telah dijalankan dan lakukan investigasi pada konsol browser. Jawab pertanyaan berikut:

    Apa yang terjadi pada konsol browser saat klien pertama kali terhubung ke server?
    Jelaskan proses pertukaran pesan antara klien dan server. Apa yang terjadi pada konsol browser saat klien mengirim pesan?
