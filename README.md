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

![image](https://github.com/user-attachments/assets/be559cfa-2fa5-475c-a165-6a2e8f9e6806)


<h2>5. Operator</h2>

        <?php
        $gaji = 1000000;
        $pajak = 0.1;
        $thp = $gaji - ($gaji*$pajak);
        echo "Gaji sebelum pajak = Rp. $gaji <br>";
        echo "Gaji yang dibawa pulang = Rp. $thp";
        ?>

![image](https://github.com/user-attachments/assets/0e395351-1991-46b9-b53a-314beb680501)

Program ini menggunakan operator aritmatika untuk menghitung gaji setelah dipotong pajak:

Menghitung pajak:
Gaji dipotong pajak 10% dengan rumus $gaji * $pajak.

Menghitung gaji yang dibawa pulang:
Gaji setelah pajak dihitung dengan $gaji - ($gaji * $pajak).
<hr> <br>

<h2>6. Kondisi IF</h2>

        <?php
        $nama_hari = date("l");
        if ($nama_hari == "Sunday") {
        echo "Minggu";
        } elseif ($nama_hari == "Monday") {
        echo "Senin";
        } else {
        echo "Selasa";
        }
        ?>

![image](https://github.com/user-attachments/assets/c73350fe-31f7-4b93-9ab0-c70db8bfa432)

Program ini menggunakan kondisi if untuk mencetak nama hari dalam bahasa Indonesia:

Jika hari adalah "Sunday", mencetak "Minggu".
Jika hari adalah "Monday", mencetak "Senin".
Jika bukan "Sunday" atau "Monday", mencetak "Selasa".
<hr> <br>

<h2>7. Kondisi Switch</h2>

        <?php
        $nama_hari = date("l"); 
        switch ($nama_hari) {
            case "Sunday":
                echo "Minggu"; 
                break;
            case "Monday":
                echo "Senin"; 
                break;
            case "Tuesday":
                echo "Selasa"; 
                break;
            case "Wednesday":
                echo "Rabu"; 
                break;
            case "Thursday":
                echo "Kamis"; 
                break;
            case "Friday":
                echo "Jumat"; 
                break;
            case "Saturday":
                echo "Sabtu"; 
                break;
            default:
                echo "Hari tidak dikenal"; 
        }
        ?>
        
![image](https://github.com/user-attachments/assets/c7cefc09-d430-4927-9d59-32f3d9dd6b3e)
  
Program menggunakan switch untuk mencetak nama hari dalam bahasa Indonesia berdasarkan nama hari dalam bahasa Inggris. Contoh: "Sunday" menjadi "Minggu," "Monday" menjadi "Senin."
<br> <hr>

<h2>8.Perulangan For</h2>

        <h2>8. Perulangan For</h2>
        
        <?php
        echo "Perulangan 1 sampai 10 <br />";
        for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
        }
        echo "Perulangan Menurun dari 10 ke 1 <br />";
        for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
        }
        ?>

![image](https://github.com/user-attachments/assets/d33c936b-92c3-4d2f-8dae-edd1efe018b0)

**Perulangan dari 1 hingga 10:**

Perulangan ini menggunakan `for` untuk mengulang dari 1 hingga 10. Pada setiap iterasi, nilai dari variabel `$i` akan ditampilkan menggunakan `echo`.

**Perulangan Menurun dari 10 ke 1:**

Perulangan ini juga menggunakan `for`, namun dimulai dari 10 dan mengurangi nilai `$i` hingga mencapai 1 (dengan menggunakan `$i--`). Hasil outputnya akan menunjukkan dua jenis perulangan:

- Perulangan yang meningkat dari 1 hingga 10.
- Perulangan yang menurun dari 10 hingga 1.
<hr> <br>

<h2>9. Perulangan While</h2>

        <?php
        echo "Perulangan 1 sampai 10 <br />";
        $i=1;
        while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
        }
        ?>

![image](https://github.com/user-attachments/assets/ac2f86dc-1012-4146-b3bd-7d359f4f5225)

        <h2>10. Perulangan Dowhile</h2>
        
        <?php
        echo "Perulangan 1 sampai 10 <br />";
        $i=1;
        do {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
        } while ($i<=10);
        ?>

![image](https://github.com/user-attachments/assets/2214c3ad-9344-48cf-9106-5624d9a940e1)

Program ini menggunakan perulangan do...while untuk menampilkan angka dari 1 hingga 10. Perulangan ini dijalankan setidaknya satu kali, karena kondisi diperiksa setelah blok perulangan dieksekusi.
<hr> <br>

<h2>Jawaban dan Tugas</h2>

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <title>Form Input</title>
        </head>
        <body>
            <h2>Form Input Data</h2>
            <!-- Form Input untuk Nama, Tanggal Lahir, dan Pekerjaan -->
            <form method="POST">
                <label>Nama: </label>
                <input type="text" name="nama" required><br><br>
        
                <label>Tanggal Lahir: </label>
                <input type="date" name="tanggal_lahir" required><br><br>
        
                <label>Pekerjaan: </label>
                <select name="pekerjaan" required>
                    <option value="Programmer">Programmer</option>
                    <option value="Designer">Designer</option>
                    <option value="Manager">Manager</option>
                    <option value="Analyst">Analyst</option>
                </select><br><br>
        
                <input type="submit" value="Kirim">
            </form>
        
            <?php
            if ($_SERVER["REQUEST_METHOD"] == "POST") {
                // Menangkap inputan pengguna
                $nama = $_POST['nama'];
                $tanggal_lahir = $_POST['tanggal_lahir'];
                $pekerjaan = $_POST['pekerjaan'];
        
                // Menghitung umur berdasarkan tanggal lahir
                $dob = new DateTime($tanggal_lahir);
                $today = new DateTime();
                $umur = $today->diff($dob)->y;
        
                // Menentukan gaji berdasarkan pekerjaan
                switch ($pekerjaan) {
                    case "Programmer":
                        $gaji = "Rp 8.000.000,-";
                        break;
                    case "Designer":
                        $gaji = "Rp 6.500.000,-";
                        break;
                    case "Manager":
                        $gaji = "Rp 12.000.000,-";
                        break;
                    case "Analyst":
                        $gaji = "Rp 7.500.000,-";
                        break;
                    default:
                        $gaji = "Tidak diketahui";
                }
        
                // Menampilkan hasil
                echo "<h3>Data Pengguna</h3>";
                echo "Nama: $nama<br>";
                echo "Tanggal Lahir: $tanggal_lahir<br>";
                echo "Pekerjaan: $pekerjaan<br>";
                echo "Umur: $umur tahun<br>";
                echo "Gaji: $gaji<br>";
            }
            ?>
        
        </body>
        </html>


![image](https://github.com/user-attachments/assets/ac560146-f1fc-45be-b3c7-66b9dd5dcb69)

Nama: Nama yang Anda isikan pada form.  
Tanggal Lahir: Tanggal lahir yang Anda masukkan.  
Umur: Umur Anda yang dihitung berdasarkan tanggal lahir hingga hari ini.  
Pekerjaan: Pekerjaan yang Anda pilih pada form.  
Gaji: Gaji sesuai dengan pekerjaan yang dipilih, ditampilkan dalam format rupiah.






