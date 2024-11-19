90<h1>PHP DASAR</h1>
<br> <hr>

<h2>1. Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut.</h2>

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>PHP Dasar</title>
    </head>
    <body>
        <h1>Belajar PHP Dasar</h1>
        <?php
            // Menampilkan teks "Hello World"
            echo "Hello World";
        ?>
    </body>
    </html>

    
![image](https://github.com/user-attachments/assets/a0069d17-4da2-407b-8e3d-0120378be7f8)


Struktur HTML: HTML menyediakan kerangka dasar untuk halaman web, termasuk elemen seperti <!DOCTYPE html>, <html>, <head>, dan <body>.

Kode PHP: Di dalam tag PHP (<?php ?>), fungsi echo digunakan untuk menampilkan teks "Hello World" di browser.
<br> <hr>

<h2>2. Menambahkan variable pada program.</h2>

        <body>
            <h2>Menggunakan Variable</h2>
        </body>
        <?php
        $nim = "312310139";
        $nama = 'Muhammad Dhean Shafwan';
        echo "NIM : " . $nim . "<br>";
        echo "Nama : $nama";
        ?>

![image](https://github.com/user-attachments/assets/5a79c418-a600-4f8e-955f-9e94468c4615)

Program ini menyediakan formulir input yang memungkinkan pengguna untuk memasukkan nama. Setelah tombol kirim ditekan, data nama akan dikirim melalui metode POST. Nilai yang diinputkan kemudian diambil menggunakan `$_POST['nama']` dan ditampilkan kembali pada halaman yang sama.
<hr> <br>


<h2>3. Predefine Variable $_GET</h2>    

        <h1>Predefine Variable</h1>
            <?php
            echo 'Selamat Datang ' . $_GET['nama'];
            ?>

![image](https://github.com/user-attachments/assets/15a1cdf7-5710-4764-bb31-6f3b1fccfb11)

Program ini menggunakan $_GET untuk mengambil nilai yang dikirim melalui URL. Misalnya, jika URL-nya seperti ?nama=John, maka program akan menampilkan "Selamat Datang John".
Contoh penggunaan:
URL: example.com/?nama=John
Output: "Selamat Datang John"
<hr> <br>

<h2>4. Membuat Form Input</h2>

        <!DOCTYPE html>
        <html lang="en">
        <head>
        <meta charset="UTF-8">
        <title>PHP Dasar</title>
        </head>
        <body>
        <h2>Form Input</h2>
        <form method="post">
        <label>Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="Kirim">
        </form>
            <?php
            echo 'Selamat Datang ' . $_POST['nama'];
            ?>
        </body>
        </html>

![image](https://github.com/user-attachments/assets/271e68b8-8708-42a2-8e81-dcb729ff361b)


<h2>Operator</h2>

        <?php
        $gaji = 1000000;
        $pajak = 0.1;
        $thp = $gaji - ($gaji*$pajak);
        echo "Gaji sebelum pajak = Rp. $gaji <br>";
        echo "Gaji yang dibawa pulang = Rp. $thp";
        ?>

![image](https://github.com/user-attachments/assets/be559cfa-2fa5-475c-a165-6a2e8f9e6806)



