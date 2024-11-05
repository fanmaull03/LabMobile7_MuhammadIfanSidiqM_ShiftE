# Ionic 8 (With Angular) Bagian 2

<h2> Screenshot <h2> <br>
<img src="https://github.com/user-attachments/assets/0f3fbb25-d819-4546-8295-47619a3b5e33" width="300">
<img src="https://github.com/user-attachments/assets/9f278e5e-c985-48da-aedb-a5b2cc51f297" width="300"> <br>
<br>

<h3>Penjelasan </h3>

1. Membuat Database dan Tabel Pengguna:

<li> Database bernama coba-ionic dibuat dengan tabel user yang memiliki kolom username dan password. </li>
<li> Data pengguna contoh (username: tes dan password: tes123 dalam bentuk MD5) dimasukkan. </li>
<br>
2. API PHP untuk Login:

<ul>File login.php dibuat untuk menangani proses autentikasi. File ini:</ul>
<li>Mengambil input JSON dari pengguna yang berisi username dan password.</li>
<li>Mencocokkan username dan password yang di-hash dengan MD5 dari data yang dimasukkan ke database.</li>
<li>Jika cocok, login berhasil, dan sistem mengembalikan respons dengan token dan status login berhasil (status_login: 'berhasil').</li>
<li>Jika tidak cocok, login gagal (status_login: 'gagal').</li>
<br>

3. Pembuatan Proyek Ionic dan Konfigurasi Autentikasi:
<li> Proyek Ionic dibuat dengan menambahkan modul untuk autentikasi.</li>
<li>Halaman login (login.page.html) memungkinkan pengguna memasukkan username dan password, dan terdapat tombol "Login" yang memanggil fungsi login() di login.page.ts.</li>
<br>

4. Fungsi Login di Ionic:
<li>Fungsi login() mengirim data username dan password ke API PHP (login.php).</li>
<li>Jika respons menunjukkan login berhasil, token dan data pengguna disimpan, dan pengguna diarahkan ke halaman home.</li>
<li>Jika login gagal, pesan notifikasi muncul sesuai kesalahan yang terjadi.</li>
<br>

5. Guard untuk Halaman yang Memerlukan Login:
<li>Guard authGuard memastikan hanya pengguna yang sudah login bisa mengakses halaman tertentu, seperti halaman home.</li>
<li>autoLoginGuard memeriksa apakah pengguna sudah login; jika sudah, diarahkan ke home, jika belum, ke halaman login.</li>


